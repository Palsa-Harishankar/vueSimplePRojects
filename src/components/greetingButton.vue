<script setup>
import { ref } from "vue";
const name = ref("Hari");
function Greet() {
  alert(`Hey ${name.value}`);
}
function say(message) {
  alert(message + " " + `${name.value}`);
}
</script>
<template>
  <div id="div1">
    <p id="po">Click button to greet</p>
    <p id="po">Topic Event Handling</p>
    <form>
      <button id="but" @click="Greet">Greet</button>
      <button id="but" @click="say('hello')">Hello</button>
      <button id="but" @click="say('Good Morning')">GoodMorning</button>
    </form>
  </div>
  <br /><br /><br /><br /><br /><br /><br /><br /><br /><br />
</template>
<style>
#po {
  margin-left: 200px;
}
</style>
