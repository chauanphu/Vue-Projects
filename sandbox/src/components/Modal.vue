<template>
  <div @click="close" class="modal-backdrop">
    <div class="modal bg-white flex flex-col shadow-md overflow-x-auto">
      <!-- Header -->
      <header class="px-5 py-3 flex justify-between relative bg-gray-200">
        <slot name="header">Default header</slot>
        <button @click="close" class="close absolute right-0 text-red-500 hover:shadow-lg">
          <span class="material-icons"> close </span>
        </button>
      </header>
      <!-- Body -->
      <section class="px-5 flex bg-white w-96">
        <slot name="body">
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Doloremque dolores autem recusandae id hic maiores ducimus vel delectus aspernatur amet!</p>
        </slot>
      </section>
      <!-- Footer -->lg
      <footer class="px-5 py-3 bg-gray-200">
        <slot name="footer">This is footer</slot>
      </footer>lg
    </div>
  </div>
</template>

<script>
export default {
  name: "Modal",
  methods: {
      close() {
          this.$emit('close')
      }
  }
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
</style>
