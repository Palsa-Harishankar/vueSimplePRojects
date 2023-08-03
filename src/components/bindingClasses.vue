<template>
    <div id="div1">
<h2 v-bind:class=" isUnderLine &&'underline'">Underlined Text</h2>
<h1 :class="isPromted && 'promte'">Promted Movie</h1>
<h2 :class="isSoldOut ? 'sold-out':'newm'">SoldOut Movie</h2>
<h1 :class="['newm','promte']">Array Binding  for classes  Promted Movie</h1>
<h2 :class="[isPromted,'promte'&& isSoldOut ? 'sold-out':'newm']">Array Condtional Expression </h2>
<h2 :class="{
    'promte':isPromted,
    'newm':!isSoldOut,
    'sold-out':isSoldOut
}">Object Condtional Expression</h2>
</div>
<br><br><br><br><br><br><br><br><br>
</template>
<script>
export default{
    data(){
        return{
        isUnderLine:true
        ,
        isPromted:false,
        isSoldOut:false
        }
    }
}
</script>
<style>
.underline{
text-decoration: underline;
}
.promte{
    font-style: italic;
}
.newm{
    color: rgb(224, 22, 214);
}
.sold-out{
    color: red;
}
</style>