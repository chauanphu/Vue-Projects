<template>
  <div class="bg-dark h-screen">
    <div class="flex h-5/6">
      <Navbar />
      <Main />
    </div>
    <div class="w-full bg-light h-1/6"></div>
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import Main from "./views/Main.vue";
export default {
  name: "App",
  components: {
    Main,Navbar
  },
};
</script>

<style>
</style>
