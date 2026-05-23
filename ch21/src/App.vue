<script setup>
import { useCssModule } from "vue";
import Hello from "./components/Hello.vue";

console.log(useCssModule());
console.log(useCssModule("classes"));
</script>

<template>
  <Hello />
  <h1 :class="$style.bgBlue">App Component</h1>
  <h1 :class="classes.bgBlue">App Component</h1>
</template>

<!-- CSS Module -->

<style module>
.bgBlue {
  background-color: blue;
}
</style>

<!-- Custom Inject Name -->

<style module="classes">
.bgBlue {
  background-color: red;
}
</style>
