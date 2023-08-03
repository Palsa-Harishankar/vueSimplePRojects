<template >
  <div id="div1">
    <p id="po">List-Keys</p>
    <form >
      <template v-for="name in data.names" :key="name">
        <h2 style="text-align: center;" >{{ name }}</h2>
   
        <!-- <hr /> -->
      </template>
    </form>
  </div>
  <br><br><br><br><br><br><br><br><br>
</template>
<script setup>
import { reactive } from "vue";
const data = reactive({
  names: ["Bruce", "Clark", "Barry"],
});
</script>
