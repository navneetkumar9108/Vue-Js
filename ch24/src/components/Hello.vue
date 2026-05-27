<script setup>
import { computed, reactive, ref } from "vue";
import Home from "./Home.vue";

// Array of string
const students = ref(["Rahul", "Sonam", "Rohit"]);

// Array of object
const employees = ref([
  {
    name: "Sumit",
    salary: 10000,
  },
  {
    name: "Kunal",
    salary: 20000,
  },
  {
    name: "Rohit",
    salary: 30000,
  },
]);

// Array of Arrays

const languages = ref([
  ["java", "android"],
  ["python", "ml"],
  ["Dart", "flutter"],
]);

// object key value pair

const course = reactive({
  title: "learn vue js",
  author: "geekyshows",
  duration: "6 month",
});

//object of objects
const frameworks = reactive({
  vuejs: { id: 1, title: "learn vue js", author: "geekyshows", fees: 100 },
  django: { id: 2, title: "learn django", author: "geekyshows", fees: 110 },
  laravel: { id: 3, title: "learn laravel", author: "geekyshows", fees: 120 },
});

// computed property

// const sGTTTO = computed(() => {
//   return employees.value.filter((employee) => employee.salary > 10001);
// });
const sGTTTO = computed(() => {
  return employees.value.filter(({ salary }) => salary > 10001);
});

// Method
function highSalary(emps) {
  return emps.filter((emp) => emp.salary > 10001);
}
</script>

<template>
  <h1>Hello Component</h1>
  <!-- <h1 v-for="student in students">{{ student }}</h1> -->
  <!-- <h1 v-for="(student, index) in students">{{ index }}{{ student }}</h1> -->
  <!-- <h1 v-for="(student, index) in students" :key="index">
    {{ index }}{{ student }}
  </h1> -->

  <!-- // Array of object -->
  <!-- <h1 v-for="employee in employees">
    {{ employee.name }}{{ employee.salary }}
  </h1> -->
  <!-- <h1 v-for="(employee, index) in employees">
    {{ index }} {{ employee.name }}{{ employee.salary }}
  </h1> -->
  <!-- <h1 v-for="(employee, index) in employees" :key="index ">
    {{ index }} {{ employee.name }}{{ employee.salary }}
  </h1> -->

  <!-- Destructuring -->
  <!-- <h1 v-for="{ name, salary } in employees">{{ name }}{{ salary }}</h1> -->
  <!-- <h1 v-for="({ name, salary }, index) in employees">
    {{ index }} {{ name }}{{ salary }}
  </h1> -->
  <!-- <h1 v-for="({ name, salary }, index) in employees" :key="index">
    {{ index }} {{ name }}{{ salary }}
  </h1> -->

  <!-- // Array of Arrays -->
  <!-- <div v-for="language in languages">
    <h1 v-for="item in language">{{ item }}</h1>
  </div> -->
  <!-- <template v-for="(language, outerIndex) in languages">
    {{ outerIndex }}
    <h1 v-for="(item, innerIndex) in language">{{ innerIndex }}{{ item }}</h1>
  </template> -->
  <!-- <template v-for="(language, outerIndex) in languages">
    <h1 v-for="(item, innerIndex) in language">
      {{ outerIndex }}{{ innerIndex }}{{ item }}
    </h1>
  </template> -->
  <!-- <template v-for="(language, outerIndex) in languages" :key="outerIndex">
    <h1 v-for="(item, innerIndex) in language" :key="innerIndex">
      {{ outerIndex }}{{ innerIndex }}{{ item }}
    </h1>
  </template> -->

  <!-- Block of multiple Element -->
  <!-- <template v-for="(language, outerIndex) in languages" :key="outerIndex">
    <h1 v-for="(item, innerIndex) in language" :key="innerIndex">
      {{ item }}
    </h1>
    <hr />
  </template> -->

  <!-- // object key value pair -->
  <!-- <h1 v-for="value in course">{{ value }}</h1> -->
  <!-- <h1 v-for="(value, key) in course">
     {{ key }} {{ value }}
  </h1> -->
  <!-- <h1 v-for="(value, key, index) in course">
    {{ index }} {{ key }} {{ value }}
  </h1> -->
  <!-- <h1 v-for="(value, key, index) in course" :key="index">
    {{ index }} {{ key }} {{ value }}
  </h1> -->

  <!-- object of objects -->

  <!-- <div v-for="framework in frameworks">
    {{ framework.id }}{{ framework.title }}{{ framework.author
    }}{{ framework.fees }}
  </div> -->
  <!-- <div v-for="framework in frameworks" :key="framework.id">
    {{ framework.id }}{{ framework.title }}{{ framework.author
    }}{{ framework.fees }}
  </div> -->
  <!-- <div v-for="{ id, title, author, fees } in frameworks" :key="id">
    {{ id }}{{ title }}{{ author }}{{ fees }}
  </div> -->
  <!-- <div v-for="framework in frameworks" :key="framework.id">
    <h1 v-for="(value, k, index) in framework">
      {{ k }}: {{ value }} {{ index }}
    </h1>
  </div> -->

  <!-- v-for with Range -->
  <!-- <h1 v-for="n in 5">{{ n }}</h1> -->
  <!-- <h1 v-for="n in 5" :key="n">{{ n }}</h1> -->

  <!-- <template v-for="n in 5" :key="n">
    <h1>Price</h1>
  </template> -->

  <!-- v-for with v-if -->
  <!-- Below Example will not work -->
  <!-- <h1
    v-for="({ name, salary }, index) in employees"
    :key="index"
    v-if="salary > 10001"
  >
    {{ name }}{{ salary }}
  </h1> -->

  <!-- Below Example will work -->
  <!-- 
  <div v-for="({ name, salary }, index) in employees" :key="index">
    <h1 v-if="salary > 10001">{{ name }}{{ salary }}</h1>
  </div> -->

  <!-- v-for with computed property -->
  <!-- <h1 v-for="employee in sGTTTO">{{ employee.name }}{{ employee.salary }}</h1> -->
  <!-- <h1 v-for="(employee, index) in sGTTTO" :key="index">
    {{ employee.name }}{{ employee.salary }}
  </h1> -->
  <!-- <h1 v-for="({ name, salary }, index) in sGTTTO" :key="index">
    {{ name }}{{ salary }}
  </h1> -->

  <!-- v-for with method -->
  <!-- <h1 v-for="({ name, salary }, index) in highSalary(employees)" :key="index">
    {{ name }}{{ salary }}
  </h1> -->

  <!-- v-for with component -->
  <!-- <Home v-for="n in 5" :key="n" /> -->

  <!-- <Home v-for="(student, index) in students" :key="index" :item="student" /> -->

  <!-- v-for of -->
  <h1 v-for="student of students">{{ student }}</h1>
</template>

<style scoped></style>
