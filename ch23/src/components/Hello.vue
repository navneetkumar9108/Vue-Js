<script setup>
import { ref } from "vue";

const isActive = ref(false);
const num = ref(2);
const type = ref("C");
</script>

<template>
  <!-- v-if directive -->
  <!-- <h1 v-if="true">True</h1>
  <h1 v-if="isActive">isActive is True</h1>
  <h1 v-if="num === 5">num is 5</h1> -->
  <!-- <h1 v-if="num > 5">num is greater then 5</h1> -->

  <!-- v-if v-else Directive -->
  <!-- <h1 v-if="isActive">isActive is True</h1>
  <h1 v-else>this is v-else</h1> -->

  <!-- v-if v-else-if v-else Directive -->
  <!-- <h1 v-if="type === 'A'">A</h1>
  <h1 v-else-if="type === 'B'">B</h1>
  <h1 v-else-if="type === 'C'">C</h1>
  <h1 v-else>Not A/B/C</h1> -->

  <!-- v-if directive on template tag -->
  <!-- <template v-if="isActive">
    <h1>Line 1</h1>
    <h1>Line 2</h1>
    <h1>Line 3</h1></template> -->

  <!-- v-if directive on div tag -->
  <!-- <div v-if="isActive">
    <h1>Line 1</h1>
    <h1>Line 2</h1>
    <h1>Line 3</h1>
  </div> -->

  <!-- v-if v-else directive on template tag -->
  <!-- <template v-if="isActive">
    <h1>Line 1</h1>
    <h1>Line 2</h1>
    <h1>Line 3</h1>
  </template>
  <template v-else>
    <h1>Line 4</h1>
    <h1>Line 5</h1>
    <h1>Line 6</h1>
  </template> -->

  <!-- v-if v-else-if v-else directive on template tag -->
  <!-- <template v-if="type === 'A'">
    <h1>Line 1</h1>
    <h1>Line 2</h1>
    <h1>Line 3</h1>
  </template>
  <template v-else-if="type === 'B'">
    <h1>Line 4</h1>
    <h1>Line 5</h1>
    <h1>Line 6</h1>
  </template>
  <template v-else-if="type === 'C'">
    <h1>Line 7</h1>
    <h1>Line 8</h1>
    <h1>Line 9</h1>
  </template>
  <template v-else>
    <h1>Line 10</h1>
    <h1>Line 11</h1>
    <h1>Line 12</h1>
  </template> -->

  <!-- v-show directive -->
  <!-- <h1 v-show="true">True</h1> -->
  <!-- <h1 v-show="isActive">isActive is True</h1> -->
  <!-- <h1 v-show="num === 5">num is 5</h1> -->
  <!-- <h1 v-show="num > 5">num is greater then 5</h1> -->

  <!-- v-show vs v-if directive -->

  <h1 v-if="false">True</h1>
  <h1 v-show="false">True</h1>
</template>

<style scoped></style>
