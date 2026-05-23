<script setup>
import { computed, reactive, ref } from "vue";

const isActive = ref(true);
const isImportant = ref(true);

const classObj = reactive({
  active: true,
  "f-bold": true,
  iText: true,
});

const myClass = computed(() => ({
  active: isActive.value,
  "f-bold": isImportant.value,
}));

const currentTabBg = ref("bg-green");
const errorClass = ref("text-red");
</script>

<template>
  <div>
    <h1 class="Text-red">hello1</h1>
    <h1 class="Text-red font-bold">hello2</h1>
    <!-- Binding Object -->
    <h1 v-bind:class="{ active: isActive }">Hello3</h1>
    <h1 :class="{ active: isActive }">Hello4</h1>

    <!--normal class & Binding Object  -->
    <h1 class="Text-red" :class="{ active: isActive }">Hello5</h1>
    <h1 :class="{ active: isActive, 'f-bold': isImportant }">Hello6</h1>
    <h1 :class="{ active: isActive, fBold: isImportant }">Hello7</h1>
    <h1 :class="classObj">Hello8</h1>
    <h1 :class="myClass">Hello9</h1>

    <!-- Binding Array -->
    <h1 :class="[currentTabBg, errorClass]">hell010</h1>
    <h1 :class="[isActive ? currentTabBg : '', errorClass]">hell011</h1>
    <h1 :class="[{ 'bg-black': isActive }, errorClass]">hell011</h1>
  </div>
</template>

<style scoped></style>
