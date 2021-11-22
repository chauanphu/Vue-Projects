<template>
  <transition name="modal-fade">
    <div v-if="isOpen" @click="close" class="modal-backdrop">
      <div
        class="
          modal
          bg-white
          flex flex-col
          shadow-md
          overflow-x-auto
          rounded-md
        "
      >
        <!-- Header -->
        <header class="px-5 py-3 flex justify-between relative bg-gray-50">
          <slot name="header">Default header</slot>
          <button
            @click="close"
            class="close p-1 text-3xl hover:shadow-lg rounded-lg"
          >
            <span class="material-icons text-md"> close </span>
          </button>
        </header>
        <!-- Body -->
        <section class="px-5 flex bg-white w-96">
          <slot name="body">
            <p>
              Lorem ipsum dolor sit amet consectetur adipisicing elit.
              Doloremque dolores autem recusandae id hic maiores ducimus vel
              delectus aspernatur amet!
            </p>
          </slot>
        </section>
        <!-- Footer -->
        <footer class="px-5 py-3 bg-gray-50">
          <slot name="footer">This is footer</slot>
        </footer>
      </div>
    </div>
  </transition>
</template>

<script>
export default {
  name: "Modal",
  data() {
    return {
      isOpen: true,
    };
  },
  methods: {
    close() {
      this.isOpen = false;
      this.$emit("close");
    },
    open() {
      this.isOpen = true;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.modal-backdrop {
  position: fixed;
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  background: rgb(0, 0, 0, 0.3);
}
.close {
  position: absolute;
  top: 0;
  right: 0;
  color: rgb(239, 68, 68);
  background: white;
  display: flex;
  justify-content: center;
  align-items: center;
}
.modal-fade-enter,
.modal-fade-leave-to {
  opacity: 0;
}

.modal-fade-enter-active,
.modal-fade-leave-active {
  transition: opacity 0.5s ease;
}
</style>
