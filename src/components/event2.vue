<script>
export default {
  data() {
    return {
      name: "sher",
      confirmName: "",
      movie:'batman',
      movieInfo:{
        name:'actor',
        actor:'kfk'
      },
      movieList:['kfg','RRR'],
      sher:''
    };
  },
  watch: {
    name(value, pre) {
      if (value.length > 4 && value > pre) alert("4 letters are enough ");
    },
    name:{
        handler(value){
        console.log("getting respose from API "+`${value}`)},
        immediate:true
    
    },
    movie:{
        handler (value){
        console.log(`getting response from the API ${value}`)
    },
    immediate:true
    },
    movieInfo:{
        handler(value){
            console.log(`getting response from the API Movie Name : ${value.name} and Actor : ${value.actor} `)
        }
        ,
        deep:true,
        immediate:true
    },
    movieList:{
        handler(value){
            console.log('getting response from the API '+`${value}`)
        },
        deep:true,
        immediate:true
    }
  },
  methods: {
    input(event) {
      this.name = event.target.value;
    },
    confirmInput() {
      this.confirmName = this.name;
    },
    alertmassage() {
      alert("do practice well ");
    },
  },
};
</script>
<template>
  <div id="div1">
    <p id="po">Event Modifiers</p>
    <form>
      <input
        v-on:input="input($event)"
        v-on:keyup.ctrl="confirmInput()"
        placeholder="Enter Your enter  name And press ctrl to seen your name"
      />

      <p>{{ confirmName }}</p>

      <button @click="alertmassage">Alert</button>

      <input type="text" v-model="movie">
      <input type="text" v-model="movieInfo.name" >
      <input type="text" v-model="movieInfo.actor" >
      <button @click.prevent="movieList.push('Telsuko')">AddMovie</button>
    </form>
  </div>
  <br /><br /><br /><br /><br /><br /><br /><br /><br />
</template>
<style>
#div1 {
  border: solid black 3px;
  border-radius: 5px;
  background-color: #f2f2f2;
  padding: 20px;
  width: 600px;
  margin-left: 250px;
}
input {
  width: 380px;
  padding: 12px 20px;
  margin: 8px 0;
  box-sizing: border-box;
}
form {
  max-width: 450px;
  margin: 30px auto;
  background: linear-gradient(
    to right,
    hsl(61, 64%, 71%),
    rgb(236, 180, 229)
  ); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */

  text-align: left;
  padding: 40px;
  border-radius: 10px;
}
</style>
