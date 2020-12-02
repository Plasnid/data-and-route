<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view @nameChanger="changerEvent"/>
  </div>
</template>

<script>
// https://forum.vuejs.org/t/passing-props-through-router-link-solved/16868/5
export default {
  data() {
    return {
      mongoName: "Albatros"
    }
  },
  methods: {
    changerEvent(e) {
      console.log(e.newName);
      console.log(this.mongoName);
      this.mongoName = e.newName;
      console.log(`I've changed: ${this.mongoName}`);
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
