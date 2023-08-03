<script setup>
import { computed, ref } from 'vue';
const array=ref([1,2,3,5,5,6,3,7,8,2,4,6,9,10,11]);
const sets = ref([
  [1, 2, 3, 4, 5],
  [6, 7, 8, 9, 10]
])
const evenNumber=computed(()=> array.value= array.value.filter((n)=>n%2==0)
)
const sort=computed(()=>array.value.sort((a, b) => a - b))
function even(){
    return array.value.filter((n)=>n%2==0)
}
function setEven(number){
return number =number.filter((n)=>n%2==0)
}
</script>
<template>
    
    <div id="div1">
<!-- 
<li v-for="num in evenNumber">{{ num }}</li> -->
<form>
    <p>Even numbers by filter()</p>
<li v-for="n in even()">{{ n }}</li>
<p>Sorting </p>
<li v-for="x in sort">{{ x }}</li>
<p>Nested for</p>
<ul v-for="number in sets">
    <li v-for="n in setEven(number)">
    <p>{{ n }}</p>
    </li>

</ul>

</form>
</div>
<br /><br /><br /><br /><br /><br /><br /><br /><br />

</template>