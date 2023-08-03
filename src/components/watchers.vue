<script setup>
import { watch } from "vue";
import { ref } from "vue";
import { reactive } from "vue";
const count = ref(0);
const fname = ref("");
const lname = ref("shankar");
const state=reactive({
    fisrtname:'',
    lastname:''
})
watch(
  count,
  (newv, oldv) => {
    console.log(newv);
    if (newv > 10 && newv > oldv) {
      alert("you crossed your limit");
    }
  },
  {
    immediate: true,
  }
);
watch(
  [fname, lname],
  (newvalue, oldvalue) => {
    console.log("new first name  value " + newvalue[0]);
    console.log("old  first name value " + oldvalue[0]);
    console.log("new last name value " + newvalue[1]);
    console.log("old  last name value " + oldvalue[1]);
  },
  {
    immediate: true,
  }
),
watch(state,function(newvalue,oldvalue){
    console.log("new first name  value " + newvalue.fisrtname);
    console.log("old  first name value " + oldvalue.fisrtname);
    console.log("new last name value " + newvalue.lastname);
    console.log("old  last name value " + oldvalue.lastname);
})
</script>
<template>
  <div id="div1">
    <p id="po"> ref Watcher  Composition API</p>
    <form>
      <button @click.prevent="count++">+</button>
      <button @click.prevent="count--">-</button>
      <input type="text" v-model="fname" placeholder="Firstname" />
      <input type="text" v-model="lname" placeholder="Lastname" />
      <P>{{ count }}</P>
    </form>
    <p id="po"> reacvtive Watcher Composition API</p>
    <form>
      
      <input type="text" v-model="state.fisrtname" placeholder="reactive Firstname" />
      <input type="text" v-model="state.lastname" placeholder="recative Lastname" />
      
    </form>
  </div>
  <br /><br /><br /><br /><br /><br /><br /><br /><br /><br />
</template>
