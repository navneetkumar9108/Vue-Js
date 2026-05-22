<script setup>
import {
  ref,
  reactive,
  isRef,
  isReactive,
  isProxy,
  unref,
  toRef,
  toRefs,
} from "vue";

let a = 10;
let b = ref(10);
let num = reactive({ count: 1 });
let student = reactive({
  name: "sonam",
  roll: 101,
});

// console.log("a:", a);
// console.log("ia a ref:", isRef(a));
// console.log("b:", b);
// console.log("ia b ref:", isRef(b));
// console.log("num:", num);
// console.log("ia num reactive:", isReactive(num));
// console.log("ia num return proxy:", isProxy(num));
// console.log("ia b reactive:", isReactive(b));
// console.log("b:", unref(b)); //mean   -> let b= isRef(b)?b.value:b;

// console.log("student:", student);
// console.log("is student Reactive", isReactive(student));
// console.log("student.name", student.name);
// console.log("is student.name Reactive", isReactive(student.name));
// console.log("is student.name Ref", isRef(student.name));

// let nameRef = toRef(student, "name");
// console.log("nameRef", nameRef);
// console.log("is nameRef Ref ", isRef(nameRef));

let studentAsRefs = toRefs(student);
console.log("after toRefs");
console.log("studentAsRefs", studentAsRefs);
console.log("is studentAsRefs.name Ref ", isRef(studentAsRefs.name));
console.log("studentAsRefs.name.value", studentAsRefs.name.value);
console.log("studentAsRefs.roll.value", studentAsRefs.roll.value);
</script>

<template>
  <div></div>
</template>

<style scoped></style>
