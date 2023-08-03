<script>
export default {
  data() {
    return {
      name: "",
      confirmName: "",
      count: 0,
      lastname: "",
    };
  },
  computed: {
    fullNameFromComputed() {
      const lastname = "shankar";
      console.log("im running");
      if (this.name == "") {
        return "";
      }
      return this.name + " " + this.lastname;
    },
  },
  methods: {
    userInput(event) {
      this.name = event.target.value;
    },
    confirmInput() {
      this.confirmName = this.name;
    },
    showAlert() {
      alert("Hey you are doing great");
    },
    resetInput() {
      this.name = "";
      this.lastname="";
    },
    fullName(lastname) {
      console.log("im running");
      if (this.name == "") {
        return "";
      }
      return this.name + " " + lastname;
    },
  },
};
</script>

<template>
  <!--v-bind:value="name" v-on:input="userInput($event)" = v-model="name"
    insted of both we can use one v-model it is 2 way binding -->
    <div id="div1"> 
        <p id="po" class="event">Computed , Methods       And EventModifiers</p>
  <form>
    <input v-model="name" v-on:keyup.ctrl="confirmInput" placeholder="Enter Your FirstName"/>
    <input v-model="lastname" placeholder="Enter Your LastName">
    <pre>{{ confirmName }}</pre>
    
    <p>Show alerts</p>
    <button @click="showAlert">Alert</button>
    <button @click.prevent="resetInput()">ResetInput</button>
    <button @click.prevent="count++">add</button>
    <button @click.prevent="count--">sub</button>
    <p>count:{{ count }}</p>
    <p>{{ name }}</p>
    <p>{{}}</p>
    <p>{{ fullNameFromComputed }}</p>
  </form>

  </div>
  <br><br><br><br><br><br><br><br><br>
</template>
<style>
p {
  color: blue;
  font-style: italic;
  font-weight: 600;
}
#div1 {
  border: solid black 3px;
  border-radius: 5px;
  background-color: #f2f2f2;
  padding: 20px;
  width: 600px;
  margin-left: 250px;
}
.event{
    margin-right:150px;
   
}

</style>
