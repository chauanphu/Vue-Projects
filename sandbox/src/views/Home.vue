<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <Modal ref="modal">

    </Modal>
    <button class="p-5 mt-3 text-green-700 hover:shadow-md" @click="$refs.modal.open()">Open Modal</button>
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
