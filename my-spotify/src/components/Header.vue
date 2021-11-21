<template>
  <div class="flex items-center justify-between">
    <!-- Backward and Forward -->
    <div class="flex items-center">
      <button
        class="
          rounded-full
          bg-black
          w-8
          h-8
          text-white
          mr-3
          flex
          justify-center
          items-center
          opacity-50
        "
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-6 w-6"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M15 19l-7-7 7-7"
          />
        </svg>
      </button>
      <button
        class="
          rounded-full
          bg-black
          w-8
          h-8
          text-white
          mr-3
          flex
          justify-center
          items-center
          opacity-50
        "
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-6 w-6"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M9 5l7 7-7 7"
          />
        </svg>
      </button>
    </div>
    <!-- Avatar -->
    <div class="flex items-center justify-center">
      <button class="bg-black text-white border-2 border-white rounded-full p-1 px-10 mr-4">
        Upgrade
      </button>
      <button class="bg-black rounded-full p-1 flex items-center">
        <img
          src="@/assets/Spotify_Icon_RGB_Green.png"
          class="rounded-full h6 w-6 mr-3"
        />
        <p class="text-white font-semibold text-xs mr-2">Phu Chau</p>
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-5 w-5 text-white"
          viewBox="0 0 20 20"
          fill="currentColor"
        >
          <path
            fill-rule="evenodd"
            d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
            clip-rule="evenodd"
          />
        </svg>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Main",
};
</script>

<style>
</style>