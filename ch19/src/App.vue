<!-- Mixing Scoped CSS and Global CSS -->

<script setup>
import Hello from "./components/Hello.vue";
import Home from "./components/Home.vue";
</script>

<template>
  <Hello />
  <Home />
  <h1 class="bg-blue">App Component</h1>
</template>
<!-- Scoped CSS -->

<style scoped>
.bg-blue {
  background-color: blue;
}
</style>

<!-- Global CSS -->
<style>
.fs-100 {
  font-size: 100px;
}
</style>
