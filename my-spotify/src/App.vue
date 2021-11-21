<template>
  <div class="bg-dark h-screen">
    <div id="above" class="flex h-5/6">
      <Navbar />
      <router-view></router-view>
    </div>
    <div id="playlist" class=" w-full bg-light h-1/6"></div>
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
export default {
  name: "App",
  components: {
    Navbar,
  },
};
</script>

<style>
#above{
  height: 90%;
}
#playlist{
  height: 10%;
}

</style>
