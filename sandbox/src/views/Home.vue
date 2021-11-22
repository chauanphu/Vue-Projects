<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <Modal />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import Modal from "@/components/Modal.vue";

export default {
  name: "Home",
  components: {
    HelloWorld,
    Modal,
  },
};
</script>
