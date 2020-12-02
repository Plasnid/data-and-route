<template>
  <div class="about">
    <h1>This is an about page {{this.$parent.mongoName}}</h1>
    <p @click="backToTop">click me!</p>
  </div>
</template>
<script>
  export default {
    methods: {
      backToTop() {
        console.log("Yep, a click has happened!");
        console.log(this.$parent.mongoName);
        this.$emit("nameChanger",{newName:"Sparrow"});
      }
    }
  }
</script>
