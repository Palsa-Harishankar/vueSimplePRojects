<script setup>
import { ref } from "vue";
const items = ref([{ message: "foo" }, { message: "boo" }]);
var parentMassage = ref("Parent");
</script>
<template>
  <div id="div1">
    <p id="po">List Rendering</p>
    <form action="">
      <li v-for="item in items">
        {{ item.message }}
      </li>

      <li v-for="(item, index) in items">
        {{ parentMassage }}- {{ index }} - {{ item.message }}
      </li>
      <!--print 1-10 -->
      <p v-for="n in 10">{{ n + " " }}</p>
      <ul>
        <template v-for="item in items">
          <li>{{ item.message }}</li>
        </template>
      </ul>
      <p>Nested V-for</p>
      <template v-for="one in 3">
        <li>{{ one }}</li>
        <li v-for="n in items">
          {{ n.message }}
        </li>
        <li v-for="number in 10">
          {{ number }}
        </li>
      </template>
    </form>
  </div>
  <br /><br /><br /><br /><br /><br /><br /><br /><br />
</template>
