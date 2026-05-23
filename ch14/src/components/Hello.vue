<script setup>
import { computed, isRef, ref } from "vue";

let firstName = ref("Navneet");
let lastName = ref("kumar");

const fullName = computed({
  get() {
    console.log("getter called");
    return firstName.value + " " + lastName.value;
  },

  set(newValue) {
    console.log("Setter called");
    [firstName.value, lastName.value] = newValue.split(" ");
  },
});

setTimeout(() => {
  console.log("setTimeout");
  fullName.value = "Rohit Kumar";
}, 2000);

console.log(isRef(fullName));
</script>

<template>
  <div>
    <h1>{{ fullName }}</h1>
  </div>
</template>

<style scoped></style>
