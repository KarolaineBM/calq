<template>
  <q-page class="row flex-center">
    <div class="col-md-5 col-xs-12 q-pa-md">
      <div class="row">
        <q-input class="full-width" outlined v-model="display"></q-input>
      </div>

      <div class="row">
        <div class="col-3">
          <q-btn
            class="full-width"
            size="lg"
            color="blue-8"
            @click="apagaTudo()"
            >AC</q-btn
          >
        </div>

        <div class="col-3">
          <q-btn
            class="full-width"
            size="lg"
            color="blue-8"
            @click="botaoMaisOuMenos()"
            >+/-</q-btn
          >
        </div>

        <div class="col-3">
          <q-btn
            class="full-width"
            size="lg"
            color="blue-8"
            @click="botaoDePorcentagem()"
            >%</q-btn
          >
        </div>

        <div class="col-3">
          <q-btn
            class="full-width"
            size="lg"
            color="blue-8"
            @click="botaoDeDivisao()"
            >/</q-btn
          >
        </div>
      </div>

      <div class="row">
        <div class="col-3">
          <q-btn
            class="full-width"
            size="lg"
            color="blue-5"
            @click="calNumeros(7)"
            >7</q-btn
          >
        </div>

        <div class="col-3">
          <q-btn
            class="full-width"
            size="lg"
            color="blue-5"
            @click="calNumeros(8)"
            >8</q-btn
          >
        </div>

        <div class="col-3">
          <q-btn
            class="full-width"
            size="lg"
            color="blue-5"
            @click="calNumeros(9)"
            >9</q-btn
          >
        </div>

        <div class="col-3">
          <q-btn
            class="full-width"
            size="lg"
            color="blue-8"
            @click="botaoDeMultiplicar()"
            >X</q-btn
          >
        </div>
      </div>

      <div class="row">
        <div class="col-3">
          <q-btn
            class="full-width"
            size="lg"
            color="blue-5"
            @click="calNumeros(6)"
            >6</q-btn
          >
        </div>

        <div class="col-3">
          <q-btn
            class="full-width"
            size="lg"
            color="blue-5"
            @click="calNumeros(5)"
            >5</q-btn
          >
        </div>

        <div class="col-3">
          <q-btn
            class="full-width"
            size="lg"
            color="blue-5"
            @click="calNumeros(4)"
            >4</q-btn
          >
        </div>

        <div class="col-3">
          <q-btn
            class="full-width"
            size="lg"
            color="blue-8"
            @click="botaoDeMenos()"
            >-</q-btn
          >
        </div>
      </div>

      <div class="row">
        <div class="col-3">
          <q-btn
            class="full-width"
            size="lg"
            color="blue-5"
            @click="calNumeros(3)"
            >3</q-btn
          >
        </div>

        <div class="col-3">
          <q-btn
            class="full-width"
            size="lg"
            color="blue-5"
            @click="calNumeros(2)"
            >2</q-btn
          >
        </div>

        <div class="col-3">
          <q-btn
            class="full-width"
            size="lg"
            color="blue-5"
            @click="calNumeros(1)"
            >1</q-btn
          >
        </div>

        <div class="col-3">
          <q-btn
            class="full-width"
            size="lg"
            color="blue-8"
            @click="botaoDeMais()"
            >+</q-btn
          >
        </div>
      </div>

      <div class="row">
        <div class="col-3">
          <q-btn
            class="full-width"
            size="lg"
            color="blue-5"
            @click="calNumeros(0)"
            >0</q-btn
          >
        </div>

        <div class="col-3">
          <q-btn
            class="full-width"
            size="lg"
            color="blue-5"
            @click="calNumeros(0)"
            >0</q-btn
          >
        </div>

        <div class="col-3">
          <q-btn
            class="full-width"
            size="lg"
            color="blue-5"
            @click="ponto()"
            label="."
          ></q-btn>
        </div>

        <div class="col-3">
          <q-btn
            class="full-width"
            size="lg"
            color="blue-8"
            @click="botaoDeCalcular()"
            >=</q-btn
          >
        </div>
      </div>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from "@vue/runtime-core";
import { ref } from "vue";

export default defineComponent({
  name: "PageTeste",

  setup() {
    //VARIAVEIS
    const display = ref("");
    const total = ref("");
    const num1 = ref("");
    const num2 = ref("");
    const primeiraAcao = ref("");
    const segundaAcao = ref("");
    const operador = ref("");

    //METODOS
    const calNumeros = (numeros) => {
      display.value = display.value + numeros;
    };

    const botaoDeMais = (adisao) => {
      num1.value = display.value;
      display.value = "";
      operador.value = "+";
    };

    const botaoDeMenos = (subtracao) => {
      num1.value = display.value;
      display.value = "";
      operador.value = "-";
    };

    const botaoDeMultiplicar = (multiplicacao) => {
      num1.value = display.value;
      display.value = "";
      operador.value = "*";
    };

    const botaoDeDivisao = (dividir) => {
      num1.value = display.value;
      display.value = "";
      operador.value = "/";
    };

    const botaoDePorcentagem = (porcentagem) => {
      num1.value = display.value;
      display.value = "";
      operador.value = "%";
    };

    const botaoMaisOuMenos = (maisoumenos) => {};

    const apagaTudo = (limpar) => {
      display.value = "";
      operador.value = "";
    };

    const ponto = () => {
      display.value = display.value + ".";
    };

    const botaoDeCalcular = (calcular) => {
      primeiraAcao.value = parseFloat(num1.value);
      segundaAcao.value = parseFloat(display.value);

      //IF (SE) PARA SABER SE É TRUE OR FALSE
      if (operador.value == "+") {
        display.value = primeiraAcao.value + segundaAcao.value;
      }

      if (operador.value == "-") {
        display.value = primeiraAcao.value - segundaAcao.value;
      }

      if (operador.value == "*") {
        display.value = primeiraAcao.value * segundaAcao.value;
      }

      if (operador.value == "/") {
        display.value = primeiraAcao.value / segundaAcao.value;
      }

      if (operador.value == "%") {
        display.value = (primeiraAcao.value * segundaAcao.value) / 100;
      }
    };

    return {
      ref,
      display,
      total,
      botaoDeMais,
      botaoDeMenos,
      botaoDeMultiplicar,
      botaoDeDivisao,
      botaoDePorcentagem,
      botaoMaisOuMenos,
      calNumeros,
      apagaTudo,
      botaoDeCalcular,
      primeiraAcao,
      segundaAcao,
      num1,
      num2,
      ponto,
    };
  },
});
</script>

<style></style>
