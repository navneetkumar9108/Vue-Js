<!-- Text Interpolation -->

<script setup>
const msg = "Learn vue from geekyShow";
const num = 10;
const on = true;
const nameCity = "Navneet Patna";
function disp() {
  console.log("Hello from Disp");
}
</script>

<template>
  <h1>Hello World</h1>
  <h2>{{ 10 + 10 }}</h2>
  <p>{{ msg }}</p>
  <h1>{{ num + 1 }}</h1>
  {{ disp() }}
  {{ on ? "dark" : "light" }}
</template>

<style lang="scss" scoped></style>
