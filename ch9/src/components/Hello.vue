<script setup lang="ts">
import { reactive } from "vue";

// without Reactivity
// let num = { a: 10, b:  20 };
// setTimeout(() => {
//   console.log("settimeout is called");
//   console.log("num", num);
//   num.a = 30;
//   console.log("a:", num.a);
// }, 2000);

// with reactivity
// let num = reactive({ a: 10, b: 20 });
// setTimeout(() => {
//   console.log("settimeout is called");
//   console.log("num", num);
//   num.a = 30;
//   console.log("a:", num.a);
// }, 2000);

// without Reactivity
// let count = 0;
// setTimeout(() => {
//   console.log("settimeout is called");
//   count++;
//   console.log("count:", count);
// }, 2000);

// with  Reactivity
// let num = reactive({ count: 0 });
// setTimeout(() => {
//   console.log("settimeout is called");
//   console.log("num", num);
//   num.count++;
//   console.log("count:", num.count);
// }, 2000);

// deep Reactivity
const obj = reactive({
  num: { count: 0 },
  user: ["Rahul", "Sonam"],
});
setTimeout(() => {
  console.log("settimeout is called");
  console.log("obj", obj);
  console.log("obj.num", obj.num);
  console.log("obj.num.count", obj.num.count);
  console.log("obj.num.user", obj.user);
  obj.num.count++;
  obj.user.push("Rohit");
  console.log("obj", obj);
  // console.log("count:", num.count);
}, 2000);
</script>
<template>
  <div>
    <!-- with or without Reactivity -->
    <!-- <h1>Sum:{{ num.a + num.b }}</h1> -->
    <!-- <h1>Count:{{ count }}</h1> -->
    <!-- <h1>Count:{{ num.count }}</h1> -->
    <h1>Count: {{ obj.num.count }}</h1>
    <h1>User:{{ obj.user }}</h1>
    <h1>User:{{ obj.user[0] }}</h1>
    <h1>User:{{ obj.user[1] }}</h1>
  </div>
</template>

<style lang="scss" scoped></style>
