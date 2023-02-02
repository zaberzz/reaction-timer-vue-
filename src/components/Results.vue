<template>
  <h1>your result is equla to : {{ score }} ms</h1>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
  props: ["score"],
  data() {
    return {
      rank: null,
    };
  },
  mounted() {
    if (this.score < 250) {
      this.rank = "You are awsome";
    } else if (this.score < 400) {
      this.rank = "you are fast";
    } else {
      ("snail speed ...");
    }
  },
};
</script>

<style>
.rank {
  font-size: 1.4em;
  color: #0faf87;
  font-weight: bold;
}
</style>
