<template>
  <div class="w-full h-full bg-dark relative overflow-y-scroll">
    <!-- Header -->
    <Header class="w-full sticky top-0 p-4"></Header>
    <main>
      <section class="px-6">
        <div class="py-3 mb-3 flex justify-between">
          <a href="#" class="text-white text-2xl font-semibold hover:underline"
            >Your top mixes</a
          >
          <a
            href="#"
            class="
              text-lightest text-sm
              hover:underline
              font-semibold
              tracking-wider
            "
            >SEE ALL</a
          >
        </div>
        <!-- Cards -->
        <div class="w-full flex flex-wrap">
          <div
            v-for="number in [1, 2, 3, 4, 5]"
            :key="number"
            class="w-52 rounded-full h-auto"
          >
            <a href="#">
              <div
                class="card hover:bg-light w-full h-auto shadow-md p-3 rounded"
              >
                <img
                  class="w-full h-auto rounded-lg mb-2"
                  src="@/assets/mixes-1.jpg"
                  alt=""
                />
                <h1 class="text-white font-semibold">6 Minute English</h1>
                <h2 class="text-gray-400 text-sm">BBC Radio</h2>
              </div>
            </a>
          </div>
        </div>
      </section>
    </main>
  </div>
</template>

<script>
import Header from "@/components/Header";

export default {
  components: { Header },
};
</script>

<style scoped>
.card {
  background-color: #181818;
}
.card:hover {
  background-color: #282828;
}
.card img {
  position: relative;
  height: 0;
  padding-bottom: 20%;
}
</style>
