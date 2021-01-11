<template>
  <div>
    {{ countDown }}
    <input v-model="hr" type="number" />
    <input v-model="min" type="number" />
    <input v-model="sec" type="number" />
    <button type="button" @click="setRunning(true)">Start</button>
    <button type="button" @click="setRunning(false)">Stop</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      hr: 0,
      min: 0,
      sec: 30,
      countDown: 0,
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
    },
    hr: function () {
      if (this.hr) {
        this.countDown += this.hr * 3600;
      }
    },
    min: function () {
      if (this.min) {
        this.countDown += this.min * 60;
      }
    },
    sec: function () {
      if (this.sec) {
        this.countDown += this.sec;
      }
    }
  },
  created() {
  
  }
};
</script>