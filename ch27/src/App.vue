<script setup>
import { ref } from "vue";
import Hello from "./components/Hello.vue";
import { Person } from "./services/Person.js";

const firstName = ref("Sonam");
const lastName = ref("Kumari");

// setTimeout(() => {
//   firstName.value = "Rahul";
// }, 3000);

// Binding Multipal Properties using an object

// const employee = {
//   name: "Rahul",
//   company: "HCL",
// };

// Custom  class
const person = new Person("Sonam", "Kumari");
</script>

<template>
  <h1>App Component</h1>
  <!-- Static Prop -->

  <!-- <Hello fullName="Sonam Kumari" /> -->
  <!-- <Hello full-name="Sonam Kumari" /> -->

  <!-- Dynamic Prop -->
  <!-- <Hello :firstName="firstName" :lastName="lastName" /> -->

  <!-- one way data flow -->
  <!-- <Hello :firstName="firstName" :lastName="lastName" /> -->

  <!-- props validation -->
  <!-- <Hello full-name="Sonam Kumari" age="27" /> -->
  <!-- <Hello full-name="Sonam Kumari" :age="27" /> -->
  <!-- <Hello full-name="Sonam Kumari" :age="27" /> -->

  <!-- Boolean Casting -->
  <!-- <Hello is-logout="true" /> -->
  <!-- <Hello :is-logout="true" /> -->
  <!-- <Hello is-logout /> -->
  <!-- <Hello /> -->

  <!-- Array and Object -->
  <!-- <Hello
    :cities="['Ranchi', 'Bokaro', 'Dhanbad']"
    :employee="{ name: 'Sonam', company: 'HCL' }"
  /> -->

  <!-- Binding Multipal Properties using an object -->
  <!-- <Hello v-bind="employee" /> -->
  <!-- <Hello name="Rahul" company="HCL" /> -->
  <!-- <Hello :name="employee.name" :company="employee.company" /> -->

  <!-- Custom Validation -->
  <!-- <Hello name="Sonam" :age="27" /> -->

  <!-- Custom Class -->
  <Hello :author="person" />
</template>

<style scoped></style>
