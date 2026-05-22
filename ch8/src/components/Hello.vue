<!-- Attribute Binding -->
<script setup>
const msg = "learn vue js by geekyShows";
const myDataId = "jack";
const url = "https://www.google.com/";

//Dynamic Binding Multiple Attributes

const objOfAttrs = {
  id: "jack",
  href: "https://www.google.com/",
};

// Dynamic Argument
const attributeName = "href";

// Boolean Attribute
const isDisabled = true;
</script>

<template>
  <div>
    <h1>{{ msg }}</h1>
    <h1 id="jack">Hello 1</h1>
    <h1 v-bind:id="myDataId">Hello 2</h1>
    <h1 :id="myDataId">Hello 3</h1>
    <a href="https://www.google.com/"> visit us</a><br />
    <a v-bind:href="url">visit us 2</a><br />
    <a :href="url">visit us 3</a><br />
    <a :href="url" :id="myDataId">visit 4</a>

    <!-- Dynamic Binding Multiple Attributes -->
    <a v-bind="objOfAttrs">visit 5</a><br />

    <!-- Dynamic Argument -->
    <a v-bind:[attributeName]="url">visit 6</a><br />
    <a :[attributeName]="url">visit 7</a><br />

    <!-- Boolean Attribute -->
    <button disabled>Click 1</button><br />
    <button :disabled="isDisabled">Click 2</button>
  </div>
</template>

<style lang="scss" scoped></style>
