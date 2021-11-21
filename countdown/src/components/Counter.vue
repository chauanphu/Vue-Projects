<template>
  <div class="shadow-md container p-10 mx-auto">
    <h1 class="text-4xl mb-2">Current Time</h1>
    <section class="flex text-6xl content-center justify-center">
      <div class="mr-2 relative">
        {{ currentTime.hour }}
        <div class="label text-sm">Hours</div>
      </div>
      <span>:</span>

      <div class="mx-2 relative">
        {{ currentTime.minute }}
        <div class="label text-sm">Minutes</div>
      </div>
      <span>:</span>

      <div class="ml-2 relative">
        {{ currentTime.second }}
        <div class="label text-sm">Seconds</div>
      </div>
    </section>

    <h1 class="text-3xl mb-2 font-bold">Timer</h1>
    <section class="flex text-6xl content-center justify-center">
      <div class="mr-2 relative">
        {{ countDown.hour }}
        <div class="label text-sm">Hours</div>
      </div>
      <span>:</span>

      <div class="mx-2 relative">
        {{ countDown.minute }}
        <div class="label text-sm">Minutes</div>
      </div>
      <span>:</span>

      <div class="ml-2 relative">
        {{ countDown.second }}
        <div class="label text-sm">Seconds</div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "Counter",
  created() {
    setInterval(() => {
      this.currentTime = this.getcurrentTime();
      this.countDown = this.cal_count_down()
    }, 1000);
  },
  data() {
    return {
      currentTime: {
        hour: "00",
        minute: "00",
        second: "00",
      },
      countDown: {
        hour: "00",
        minute: "00",
        second: "00",
      },
    };
  },
  methods: {
    getcurrentTime() {
      const time = new Date();
      const hour =
        time.getHours() < 10 ? "0" + time.getHours() : time.getHours();
      const minute =
        time.getMinutes() < 10 ? "0" + time.getMinutes() : time.getMinutes();
      const second =
        time.getSeconds() < 10 ? "0" + time.getSeconds() : time.getSeconds();
      return { hour, minute, second };
    },
    cal_count_down() {
      const now = new Date()

      const _hour = 23 - now.getHours()
      const _minute = 60 - now.getMinutes()
      const _second = 60 - now.getSeconds()

      const hour =
        _hour < 10 ? "0" + _hour : _hour;
      const minute =
        _minute < 10 ? "0" + _minute : _minute;
      const second =
        _second < 10 ? "0" + _second : _second;
      return { hour, minute, second };
    }
  },
};
</script>

<style>
section {
  margin-bottom: 1em;
}
</style>