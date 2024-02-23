<script setup>
import { ref } from "vue";

const first = ref(0);
const second = ref(0);
const result = ref(0);

const addition = () => {
  result.value = Number(first.value) + Number(second.value);
}

const subtraction = () => {
  result.value = Number(first.value) - Number(second.value);
}

const multiplication = () => {
  result.value = Number(first.value) * Number(second.value);
}

const division = () => {
  result.value = Number(first.value) / Number(second.value);
}

const refreshpage = () => {
  window.location.reload();
}

</script>

<template>
  <main>
    <br>
    <h1>Calculator</h1><br>
    <div>
      <p>first number:</p><input v-model="first" type="number">
      <p>second number:</p><input v-model="second" type="number"><br>
      <div class="buttons-div">
        <button @click="addition">+</button>
        <button @click="subtraction">-</button>
        <button @click="multiplication">*</button>
        <button @click="division">/</button>
      </div>
      <h2>Result: {{ result }}</h2>
      <button class="button" @click="refreshpage">Clear</button>
    </div>
  </main>
</template>