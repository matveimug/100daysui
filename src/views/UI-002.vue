<template>
  <div>
    {{ countDown }}
    <input v-model="countDown" type="number" />
    <button type="button" @click="setRunning(true)">Start</button>
    <button type="button" @click="setRunning(false)">Stop</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      countDown: 60,
      running: false,
    };
  },
  methods: {
    setRunning(bool) {
      this.running = bool;
    },
    countDownTimer() {
      if (this.countDown > 0 && this.running) {
        setTimeout(() => {
          this.countDown -= 1;
          this.countDownTimer();
        }, 1000);
      }
    },
  },
  watch: {
    running: function () {
      this.countDownTimer();
    }
  },
  created() {
  
  }
};
</script>