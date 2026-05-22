<script setup>
import { reactive, ref } from "vue";

//  without reactivity
// let a = 10;
// let b = 20;

// setTimeout(() => {
//   console.log("setTimeout is called");
//   a = 30;
// }, 2000);

// with reactivity
// let a = ref(10);
// let b = ref(20);

// setTimeout(() => {
//   console.log("setTimeout is called");
//   console.log("a", a);
//   console.log("b", b);
//   console.log("a.value", a.value);
//   console.log("b.value", b.value);
//   a.value = 30;
// }, 2000);

// without reactivity
// let count = 0;
// setTimeout(() => {
//   console.log("setTimeout is called");
//   count++;
// }, 2000);

// with reactivity
// let count = ref(0);
// setTimeout(() => {
//   console.log("setTimeout is called");
//   count.value++;
// }, 2000);

// object
// let obj1 = ref({ count: 0 });
// setTimeout(() => {
//   console.log("setTimeout is called");
//   console.log("obj1", obj1);
//   console.log("obj1.value", obj1.value);
//   console.log("obj1.value.count", obj1.value.count);
//   obj1.value.count++;
//   console.log("obj1.value.count", obj1.value.count);
// }, 2000);

// let obj2 = { count: ref(0) };
// let { count } = obj2;
// setTimeout(() => {
//   console.log("setTimeout is called");
//   console.log("obj2", obj2);
//   console.log("obj2.count", obj2.count);
//   console.log("obj2.count.value", obj2.count.value);
//   obj2.count.value++;
//   console.log("obj2.count.value", obj2.count.value);
// }, 2000);

// let obj3 = ref({ count: ref(0) });
// let { count } = obj3;
// setTimeout(() => {
//   console.log("setTimeout is called");
//   console.log("obj3", obj3);
//   console.log("obj3.value", obj3.value);
//   console.log("obj3.value.count", obj3.value.count);
//   obj3.value.count++;
//   console.log("obj3.value.count", obj3.value.count);
// }, 2000);

// Array
const students = reactive([ref("Rahul"), ref("Sonem")]);
setTimeout(() => {
  console.log("setTimeout is called");
  console.log("students", students);
  console.log("students.[0]", students[0]);
  console.log("students.[1]", students[1]);
  console.log("students.[0].value", students[0].value);
  console.log("students.[1].value", students[1].value);
  students.push(ref("rohit"));
  console.log("students.[2].value", students[2].value);
}, 2000);
</script>

<template>
  <!-- <div>{{ a + b }}</div> -->
  <!-- <h1>{{ count }}</h1> -->
  <!-- <h1>{{ obj1.count }}</h1> -->

  <!-- <h1>{{ obj2.count }}</h1>
  <h1>{{ obj2.count.value }}</h1>
  <h1>{{ obj2.count.value + 5 }}</h1> -->
  <!-- <h1>{{ obj2.count + 5 }}</h1> it wont work -->
  <!-- <h1>{{ count + 5 }}</h1> -->

  <!-- <h1>{{ obj3.count }}</h1> -->

  <h1>{{ students }}</h1>
</template>

<style scoped></style>
