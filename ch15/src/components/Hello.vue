<!-- Binding Inline Style -->
<script setup>
import { reactive, ref } from "vue";

const cl = ref("red");
const bg = ref("yellow");

const styleObj = reactive({
  color: " red",
  backgroundColor: "blue",
});

const myStyle = reactive({
  fontSize: "100px",
});
</script>

<template>
  <div>
    <h1 style="color: red; background-color: blueviolet">Hello1</h1>
    <h1 v-bind:style="{ color: 'red', backgroundColor: 'green' }">Hello2</h1>
    <h1 v-bind:style="{ color: 'red', 'background-color': 'yellow' }">
      Hello3
    </h1>
    <h1 :style="{ color: 'red', backgroundColor: 'green' }">Hello4</h1>
    <h1 :style="{ color: 'red', 'background-color': 'yellow' }">Hello5</h1>

    <!-- Binding to object -->

    <h1 :style="{ color: cl, backgroundColor: bg }">Hello6</h1>
    <h1 :style="styleObj">Hello7</h1>

    <!-- Binding to Array -->
    <h1 :style="[styleObj, myStyle]">Hello8</h1>
  </div>
</template>

<style scoped></style>
