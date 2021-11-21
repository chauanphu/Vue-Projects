<template>
  <main>
    <nav-bar class="mb-10"></nav-bar>
    <hello-world></hello-world>
  </main>
</template>

<script>
import HelloWorld from "./views/HelloWorld.vue";
import NavBar from './components/Navbar.vue'

export default {
  name: "App",
  components: {
    HelloWorld,
    NavBar
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
