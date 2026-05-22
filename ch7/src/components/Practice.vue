<script setup>
const nameCity = "Navneet Patna";
const userDetail = { name: "Navneet", age: 24 };
const name = "navneet";
const price = 100;
const isLoggedIn = true;
const discount = 20;
const firstName = "Navneet";
const lastName = "kumar";
const numArr = [1, 2, 3];
const num = 20;
</script>

<template>
  <div>
    <h1>{{ nameCity }}</h1>
    <h1>{{ userDetail.name }}{{ " " }}{{ userDetail.age }}</h1>
    <h1>{{ 30 + 85 }}</h1>
    <h1>{{ name.toUpperCase() }}</h1>
    <h1>final prise{{ price - discount }}</h1>
    <h1>{{ isLoggedIn ? "welcome" : "please login" }}</h1>
    <h1>{{ firstName + " " + lastName }}</h1>
    <h1>{{ numArr[0] }}</h1>
    <h1>{{ String(num) }}</h1>
    <h1>{{ num.toString() }}</h1>
    <h1>{{ `${num}` }}</h1>
  </div>
</template>

<style lang="scss" scoped></style>
