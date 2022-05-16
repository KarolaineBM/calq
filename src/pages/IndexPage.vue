<template>
<!-- Bruno Teste -->
  <q-page class="flex flex-center">
    <div row items-start>
      <q-card class="my-card">
        <q-input id="resultado"></q-input>

        <div class="row">
          <div class="col-3">
            <q-btn class="q-ma-md" label="7" @click="num(7)"> </q-btn>
          </div>
          <div class="col-3">
            <q-btn class="q-ma-md" label="8" @click="num(8)"> </q-btn>
          </div>
          <div class="col-3">
            <q-btn class="q-ma-md" label="9" @click="num(9)"> </q-btn>
          </div>
          <div class="col-3">
            <q-btn class="q-ma-md" label="/" @click="out('/')"> </q-btn>
          </div>
        </div>

        <div class="row">
          <div class="col-3">
            <q-btn class="q-ma-md" label="6" @click="num(6)"> </q-btn>
          </div>
          <div class="col-3">
            <q-btn class="q-ma-md" label="5" @click="num(5)"> </q-btn>
          </div>
          <div class="col-3">
            <q-btn class="q-ma-md" label="4" @click="num(4)"> </q-btn>
          </div>
          <div class="col-3">
            <q-btn class="q-ma-md" label="*" @click="out('*')"> </q-btn>
          </div>
        </div>

        <div class="row">
          <div class="col-3">
            <q-btn class="q-ma-md" label="3" @click="num(3)"> </q-btn>
          </div>
          <div class="col-3">
            <q-btn class="q-ma-md" label="2" @click="num(2)"> </q-btn>
          </div>
          <div class="col-3">
            <q-btn class="q-ma-md" label="1" @click="num(1)"> </q-btn>
          </div>
          <div class="col-3">
            <q-btn class="q-ma-md" label="-" @click="out('-')"> </q-btn>
          </div>
        </div>

        <div class="row">
          <div class="col-3">
            <q-btn class="q-ma-md" label="0" @click="num(0)"> </q-btn>
          </div>
          <div class="col-3">
            <q-btn class="q-ma-md" label="=" @click="calcular()"> </q-btn>
          </div>
          <div class="col-3">
            <q-btn class="q-ma-md" label="C" @click="clean()"> </q-btn>
          </div>
          <div class="col-3">
            <q-btn class="q-ma-md" label="+" @click="out('+')"> </q-btn>
          </div>
        </div>
      </q-card>
    </div>
  </q-page>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    const resultado = ref(null);

    const num = (numeros) => {
      resultado.value = num1.value + num2.value;
      console.log(resultado.value);
    };

    var num1 = () => {
      num;
    };

    var num2 = () => {
      num;
    };

    const out = (outros) => {};

    const calcular = (igual) => {};

    const clean = (apagar) => {};

    return {
      num1,
      num2,
      num,
      out,
      calcular,
      clean,
      resultado,
    };
  },
};
</script>
