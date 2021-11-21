<template>
  <div class="shadow-md container p-10 mx-auto">
    <h1 class="text-4xl mb-2">Current Time</h1>
    <section class="flex text-6xl content-center justify-center">
      <div class="mr-2 relative">
        00
        <div class="label text-sm">Days</div>
      </div>
      <span>:</span>
      <div class="mx-2 relative">
        00
        <div class="label text-sm">Hours</div>
      </div>
      <span>:</span>

      <div class="mx-2 relative">
        00
        <div class="label text-sm">Minutes</div>
      </div>
      <span>:</span>

      <div class="ml-2 relative">
        00
        <div class="label text-sm">Seconds</div>
      </div>
    </section>

    <h1 class="text-3xl mb-2 font-bold">Timer</h1>
    <section class="flex text-6xl content-center justify-center">
      <div class="mr-2 relative">
        00
        <div class="label text-sm">Days</div>
      </div>
      <span>:</span>
      <div class="mx-2 relative">
        00
        <div class="label text-sm">Hours</div>
      </div>
      <span>:</span>

      <div class="mx-2 relative">
        00
        <div class="label text-sm">Minutes</div>
      </div>
      <span>:</span>

      <div class="ml-2 relative">
        00
        <div class="label text-sm">Seconds</div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "Counter",
  computed: {
    helloworld() {

    }
  }
};
</script>

<style>
section {
  margin-bottom: 1em;
}
</style>