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
            label="+/-"
          ></q-btn>
        </div>

        <div class="col-3">
          <q-btn class="full-width" size="lg" color="blue-8" label="%"></q-btn>
        </div>

        <div class="col-3">
          <q-btn class="full-width" size="lg" color="blue-8" label="/"></q-btn>
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
          <q-btn class="full-width" size="lg" color="blue-8" label="X"></q-btn>
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
          <q-btn class="full-width" size="lg" color="blue-8" label="-"></q-btn>
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
          <q-btn class="full-width" size="lg" color="blue-5" label="."></q-btn>
        </div>

        <div class="col-3">
          <q-btn class="full-width" size="lg" color="blue-8" label="="></q-btn>
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
    //variaveis
    let display = ref("");
    const total = ref("");

    //metodos
    const calNumeros = (numeros) => {
      display.value = display.value + numeros;
    };

    const botaoDeMais = () => {
      display.value = display.value;
    };

    const apagaTudo = () => {};

    return {
      ref,
      //valorTotal,
      display,
      botaoDeMais,
      calNumeros,
      apagaTudo,
    };
  },
});
</script>

<style></style>
