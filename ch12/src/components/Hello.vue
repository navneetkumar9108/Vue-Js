<!-- Method -->
<script setup>
import { ref } from "vue";

// without Ref
// let firstName = "Navneet";
// let lastName = "Kumar";

// // Method
// function fullName() {
//   return firstName + " " + lastName;
// }

// setTimeout(() => {
//   console.log("setTimeout called");
//   firstName = "Rahul";
//   console.log(firstName);
// }, 2000);
// with Ref
let firstName = ref("Navneet");
let lastName = ref("Kumar");

// Method
// function fullName() {
//   return firstName.value + " " + lastName.value;
// }

// const fullName = () => {
//   return firstName.value + " " + lastName.value;
// };
const fullName = (roll) => {
  return firstName.value + " " + lastName.value + " " + "Roll:" + " " + roll;
};

setTimeout(() => {
  console.log("setTimeout called");
  firstName.value = "Rahul";
  console.log(firstName);
}, 2000);
</script>

<template>
  <div>
    <!-- <h1>{{ fullName() }}</h1> -->
    <h1>{{ fullName(101) }}</h1>
  </div>
</template>

<style scoped></style>
