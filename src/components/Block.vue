<template>
  <div class="block" v-if="showBolck" @click="stopTimer">Click me</div>
</template>

<script>
export default {
  name: "Block",
  data() {
    return { showBolck: false, timer: null, reactionTime: 0 };
  },
  props: ["delay"],
  mounted() {
    setTimeout(() => {
      this.showBolck = true;
      this.startTimer();
    }, this.delay);
  },
  methods: {
    startTimer() {
      this.timer = setInterval(() => {
        this.reactionTime += 10;
      }, 10);
    },
    stopTimer() {
      clearInterval(this.timer);
    },
  },
};
</script>

<style>
.block {
  widows: 400px;
  border-radius: 20px;
  background-color: #0faf87;
  color: white;
  text-align: center;
  padding: 100px 0;
  margin: 40px auto;
}
</style>
