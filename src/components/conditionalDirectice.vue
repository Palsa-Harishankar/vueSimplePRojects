<script setup>
import { ref } from "vue";
const awesome = ref(true);
const num=ref(-9)
const m=ref("hey")
</script>
<template>
  <div id="div1">
    <p id="po">Conditional Rendering</p>
    <form>
        
      <button @click.prevent="awesome = !awesome" id="but">toogle❤️</button>
      <h1 v-if="awesome" style="background-color: ">
        VUE is to good FrameWork
      </h1>
      <h5 v-else>Java script is Better then VUE</h5>
      <p :title="m">hover me to get the message</p>
    </form
    >
    <h1 v-if="num===1">The Number is 0</h1>
    <h1 v-else-if="num>0">The Number is Positive</h1>
    <h1 v-if="num<0">The Number is Negitive</h1>
    <h1 v-else>this  is somthing not a number </h1>
  </div>
  <br /><br /><br /><br /><br /><br /><br /><br /><br />
</template>

<style>
button {
  color: #fff;
  background: #b9cfc8; /* fallback for old browsers */
  background: -webkit-linear-gradient(
    to right,
    #185a9d,
    #43cea2
  ); /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(
    to right,
    hsl(0, 75%, 42%),
    #2cec05e8
  ); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
    
  border: none;
  padding: 5px 10px;
  margin: 5px;
  border-radius: 8px;
  cursor: pointer;
}
button:hover{
    color: #fff;

  background: #3f3d3c; /* fallback for old browsers */
  background: -webkit-linear-gradient(
    to right,
    #b5e6b3,
    #ce4343
  ); /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(
    to right,
    hsl(290, 52%, 80%),
    #ce4aaf
  ); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
    
  border: none;
  padding: 5px 10px;
  margin: 5px;
  border-radius: 8px;
  cursor: pointer;
}




</style>
