<script setup>
import { reactive } from "vue";
const obj = reactive({
  title: "How to do lists in Vue",
  author: "Jane Doe",
  publishedAt: "2016-04-10",
});
const my_owm = reactive({
  name: "shankar",
  branch: "mech --> cse ",
  rank: "topRank",
});
</script>
<template>
  <div id="div1">
    <p id="po">Object List Rendering</p>
    <form>
      <li v-for="(values, keys) in obj">{{ keys }} : {{ values }}</li>

      <li v-for="(value, keys) in my_owm">
        {{ keys + " " }}:{{ " " + value }}
      </li>
    </form>
  </div>
</template>
