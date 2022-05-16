<template>
  <q-page class="row flex-center">
    <div class="col-md-5 col-xs-12 q-pa-md">
      <div class="row">
        <q-input class="full-width" outlined> </q-input>
      </div>

      <div class="row">
        <div class="col-3">
          <q-btn
            class="full-width"
            size="lg"
            color="blue-8"
            id="display"
          ></q-btn>
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
          <q-btn class="full-width" size="lg" color="blue-5" label="7"></q-btn>
        </div>

        <div class="col-3">
          <q-btn class="full-width" size="lg" color="blue-5" label="8"></q-btn>
        </div>

        <div class="col-3">
          <q-btn class="full-width" size="lg" color="blue-5" label="9"></q-btn>
        </div>

        <div class="col-3">
          <q-btn class="full-width" size="lg" color="blue-8" label="X"></q-btn>
        </div>
      </div>

      <div class="row">
        <div class="col-3">
          <q-btn class="full-width" size="lg" color="blue-5" label="6"></q-btn>
        </div>

        <div class="col-3">
          <q-btn class="full-width" size="lg" color="blue-5" label="5"></q-btn>
        </div>

        <div class="col-3">
          <q-btn class="full-width" size="lg" color="blue-5" label="4"></q-btn>
        </div>

        <div class="col-3">
          <q-btn class="full-width" size="lg" color="blue-8" label="-"></q-btn>
        </div>
      </div>

      <div class="row">
        <div class="col-3">
          <q-btn class="full-width" size="lg" color="blue-5" label="3"></q-btn>
        </div>

        <div class="col-3">
          <q-btn class="full-width" size="lg" color="blue-5" label="2"></q-btn>
        </div>

        <div class="col-3">
          <q-btn class="full-width" size="lg" color="blue-5" label="1"></q-btn>
        </div>

        <div class="col-3">
          <q-btn class="full-width" size="lg" color="blue-8" label="+"></q-btn>
        </div>
      </div>

      <div class="row">
        <div class="col-3">
          <q-btn class="full-width" size="lg" color="blue-5" label="0"></q-btn>
        </div>

        <div class="col-3">
          <q-btn class="full-width" size="lg" color="blue-5" label="0"></q-btn>
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
    return {};
  },
});
</script>

<style></style>
