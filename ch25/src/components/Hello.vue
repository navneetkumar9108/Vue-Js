<script setup>
import { ref } from "vue";

// <!-- // Event Handling - Inline Handlers -->
const count = ref(0);

// Calling Methods
// function say() {
//   console.log("Hello...");
// }

// function say(str) {
//   console.log(str);
// }

// Accessing Event Argument
// function say(e) {
//   console.log("event", e);
// }

// function say(str, e) {
//   console.log("Str", str);
//   console.log("Event", e);
// }

// Event Handling - Method Handlers
// function say(e) {
//   console.log("event", e);
// }

// Event Modifiers
// function checkData() {
//   console.log("check data");
// }

// function onSubmit() {
//   console.log("form Submitted");
// }

// Key Modifiers
// function onPressEnter() {
//   console.log("enter key pressed");
// }

// System Modifiers

// function onPressAltEnter() {
//   console.log("alt+enter key pressed");
// }

// function onCtrlClick() {
//   console.log("ctrl+click pressed");
// }

// function onPressCtrl() {
//   console.log("ctrl key pressed");
// }

// Exact Modifiers

// function onCtrlClick() {
//   console.log("ctrl + click pressed");
// }

// function onExactCtrlClick() {
//   console.log("Exact ctrl + click pressed");
// }

// function onNoSys() {
//   console.log("No system modifiers are pressed");
// }

// Mouse Button Modifier
// function onRightClick() {
//   console.log("right click");
// }

// Multiple Events

// function onMouseDown() {
//   console.log("mouse Down");
// }
// function onMouseUp() {
//   console.log("mouse Up");
// }

function firstEvent() {
  console.log("first event");
}

function secondEvent() {
  console.log("second event");
}
</script>

<template>
  <h1>Hello Component</h1>
  <!-- <h1>Count: {{ count }}</h1> -->
  <!-- <button v-on:click="count++">Increase</button> -->
  <!-- <button @click="count++">Increase</button> -->
  <!-- <input type="text" v-on:focusin="count++" /> -->
  <!-- <input type="text" @focusout="count--" /> -->

  <!-- calling Methods -->
  <!-- <button @click="say()">Click</button> -->
  <!-- <button @click="say('Bey...')">Click</button> -->

  <!-- Accessing Event Argument using $event Special Variable -->
  <!-- <button @click="say($event)">Click</button> -->
  <!-- <button @click="say('Hello', $event)">Click</button> -->

  <!-- Accessing Event Argument using Inline Arrow Function -->
  <!-- <button @click="(event) => say(event)">Click</button> -->
  <!-- <button @click="(event) => say('Hello', event)">Click</button> -->

  <!-- Event Handling - Method Handlers -->
  <!-- <button @click="say">Click</button> -->

  <!-- Event Modifiers -->
  <!-- <a @click="checkData" href="https://wwww.google.com">Go to Google</a> -->
  <!-- <a @click.prevent="checkData" href="https://wwww.google.com">Go to Google</a> -->
  <!-- <form @submit="onSubmit">
    <button type="submit">Submit</button>
  </form> -->
  <!-- <form @submit.prevent="onSubmit">
    <button type="submit">Submit</button>
  </form> -->
  <!-- <form @submit.prevent>
    <button type="submit">Submit</button>
  </form> -->

  <!-- Key Modifiers -->
  <!-- <input type="text" @keyup.enter="onPressEnter" /> -->

  <!-- System Modifires -->
  <!-- <input type="text" @keyup.alt.enter="onPressAltEnter" /> -->
  <!-- <input type="text" @click.ctrl="onCtrlClick" /> -->
  <!-- keyup.ctrl will only trigger if you release a key while holding down ctrl. It won't trigger if you release the ctrl key alone. -->
  <!-- <input type="text" @keyup.ctrl="onPressCtrl" /> -->

  <!-- exact Modifier -->
  <!-- <button @click.ctrl="onCtrlClick">Click</button> -->
  <!-- <button @click.ctrl.exact="onExactCtrlClick">Click</button> -->
  <!-- <button @click.exact="onNoSys">Click</button> -->

  <!-- Mouse Button Modifiers -->
  <!-- <input type="text" @click.right="onRightClick" /> -->

  <!-- Multiple Events -->
  <!-- <button v-on="{ mousedown: onMouseDown, mouseup: onMouseUp }">Click</button> -->
  <button @click="(firstEvent(), secondEvent())">Click</button>
</template>

<style scoped></style>
