<!-- Computed Property -->
<script setup>
import { computed, ref } from "vue";

// let firstName = "Navneet";
// let lastName = "Kumar";

// // computed property

// const fullName = computed(() => {
//   return firstName + " " + lastName;
// });

// setTimeout(() => {
//   console.log("setTimeout called");
//   console.log("fullName", fullName);
//   firstName = "Rohit";
//   console.log(firstName);
// }, 2000);

let firstName = ref("Navneet");
let lastName = ref("Kumar");

// computed property

const fullName = computed(() => {
  console.log("getter call");
  return firstName.value + " " + lastName.value;
});

setTimeout(() => {
  console.log("setTimeout called");
  console.log("fullName", fullName);
  firstName.value = "Rohit";
  console.log(firstName.value);
}, 2000);
</script>

<template>
  <div>
    <h1>{{ fullName }}</h1>
  </div>
</template>

<style scoped></style>
