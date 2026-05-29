<script setup>
import { Person } from "@/services/Person";
import { computed, ref } from "vue";

// const props = defineProps(["fullName"]);
// const props = defineProps(["full-name"]);

// const props = defineProps(["firstName", "lastName"]);
// console.log(props);

// don't do this because props are readonly
// props.firstName = "rohit";

// you can use it as local data property but it is disconnected from future props updates
// const fName = ref(props.firstName);

// you can use it in computed property ,it auto-update when the prop change
// const fullName = computed(() => props.firstName + "" + props.lastName);

// props validation
// const props = defineProps(["fullName", "age"]); // Don't do this

// const props = defineProps({
//   fullName: String,
//   age: Number,
// });
// const props = defineProps({
//   fullName: {
//     type: String,
//     required: true,
//     default: "Sonam Sharma",
//   },
//   age: Number,
// });

//   Boolean Casting

// const props = defineProps({
//   isLogout: Boolean,
// });

//   <!-- Array and Object -->
// const props = defineProps({
//   cities: Array,
//   employee: Object,
// });

// Binding Multipal Properties using an object
// const props = defineProps({
//   name: String,
//   company: String,
// });

// Custom Validation
// const props = defineProps({
//   name: {
//     type: String,
//     // validator(propValue) {
//     //   return ["Sonam", "Rahul", "Sumit"].includes(propValue);
//     // },
//     validator: (propValue) => ["Sonam", "Rahul", "Sumit"].includes(propValue),
//   },
//   age: {
//     type: Number,
//     // validator: (propValue) => propValue > 0,
//     validator: (propValue) => {
//       if (propValue >= 18 && propValue <= 30) {
//         return true;
//       }
//       return false;
//     },
//   },
// });

// Custom Class
const props = defineProps({
  //   author: Person,
  author: {
    type: Person,
    required: true,
  },
});
</script>

<template>
  <h1>Hello Component</h1>
  <!-- Static Prop -->

  <!-- <h1>Name: {{ fullName }}</h1> -->
  <!-- <h1>Name: {{ fullName }}</h1> -->
  <!-- <h1>{{ firstName }} {{ lastName }}</h1> -->

  <!-- <h1>{{ firstName }} {{ lastName }}</h1> -->

  <!-- <h1>f Name: {{ fName }}</h1> -->

  <!-- <h1>Full Name: {{ fullName }}</h1> -->

  <!-- <h1>First Name:{{ firstName }}</h1>
  <h1>F Name:{{ fName }}</h1>
  <h1>Full Name:{{ fullName }}</h1> -->

  <!-- props validation -->
  <!-- <h1>Name:{{ fullName }} Age:{{ age }}</h1> -->
  <!-- <h1>Name:{{ fullName }} Age:{{ age + 2 }}</h1> -->

  <!-- //   Boolean Casting -->
  <!-- <h1>isLogout: {{ isLogout }}</h1> -->

  <!-- Array and Object -->
  <!-- <h1>{{ cities }}</h1> -->
  <!-- <h1 v-for="city in cities">{{ city }}</h1> -->
  <!-- <h1>{{ employee.name }} {{ employee.company }}</h1> -->

  <!-- Binding Multipal Properties using an object -->
  <!-- <h1>Employee:{{ name }}{{ company }}</h1> -->

  <!-- Custom Validation -->
  <!-- <h1>name:{{ name }} Age:{{ age }}</h1> -->

  <!-- Custom Class -->
  <h1>Author:{{ author.firstName }}{{ author.lastName }}</h1>
</template>

<style scoped></style>
