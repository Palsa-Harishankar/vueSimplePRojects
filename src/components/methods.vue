<script>
export default {
  data() {
    return {
      count: 0,
    };
  },
  methods: {
    //method for add opertaion
    add() {
      this.count = this.count + 1;
    },
    //method for sub operation
    sub() {
      if (this.count > 0) {
        this.count = this.count - 1;
      }
    },
  },
};
</script>
<template>
    <div id="div1">
        <p id="po">
            Methods Example
        </p>
  <form>
    <!--for below event we have to create the method for ADD operation -->
    <p>Before add method count++ we are perform add operation in HTML</p>
    <button @click.prevent="count++">Add</button>
    <p>after methods</p>
    <button @click.prevent="add">addMethod</button>
    <br />
    <p>Before sub method count-- we are perform sub operation in HTML</p>
    <button @click.prevent="count--">sub</button>
    <p>after methods</p>
    <button @click.prevent="sub">subMethod</button>
    <p>{{ count }}</p>
  </form>
</div>
<br><br><br><br><br><br><br><br><br>
</template>
