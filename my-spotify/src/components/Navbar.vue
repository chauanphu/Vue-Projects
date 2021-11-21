<template>
  <div class="text-white">
    <!-- Side Nav -->
    <aside class="bg-black w-56 h-full flex-none">
      <!-- Brand -->
      <div class="p-6">
        <img
          src="@/assets/Spotify_Logo_RGB_White.png"
          alt="Spotify Logo"
          class="h-10"
        />
      </div>
      <!-- Main Buttons -->
      <div class="main-button mx-2 mb-2">
        <button
          v-for="button in mainbuttons"
          :key="button.text"
          href="#"
          class="w-full rounded px-3 py-2 flex items-start justify-start"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-6 w-6 mr-3 text-gray-300"
            viewBox="0 0 20 20"
            fill="currentColor"
            v-html="button.icon"
          ></svg>
          <p class="bg text-gray-300">{{ button.text }}</p>
        </button>
      </div>
    </aside>
  </div>
</template>

<script>
export default {
  name: "Navbar",
  data() {
    return {
      mainbuttons: [
        {
          text: "Home",
          icon: '<path d="M10.707 2.293a1 1 0 00-1.414 0l-7 7a1 1 0 001.414 1.414L4 10.414V17a1 1 0 001 1h2a1 1 0 001-1v-2a1 1 0 011-1h2a1 1 0 011 1v2a1 1 0 001 1h2a1 1 0 001-1v-6.586l.293.293a1 1 0 001.414-1.414l-7-7z"/>',
        },
        {
          text: "Search",
          icon: '<path fill-rule="evenodd" d="M8 4a4 4 0 100 8 4 4 0 000-8zM2 8a6 6 0 1110.89 3.476l4.817 4.817a1 1 0 01-1.414 1.414l-4.816-4.816A6 6 0 012 8z" clip-rule="evenodd" />',
        },
        {
          text: "Library",
          icon: '<path d="M2 4a1 1 0 011-1h2a1 1 0 011 1v12a1 1 0 01-1 1H3a1 1 0 01-1-1V4zM8 4a1 1 0 011-1h2a1 1 0 011 1v12a1 1 0 01-1 1H9a1 1 0 01-1-1V4zM15 3a1 1 0 00-1 1v12a1 1 0 001 1h2a1 1 0 001-1V4a1 1 0 00-1-1h-2z" />',
        },
      ],
    };
  },
};
</script>

<style>
</style>
