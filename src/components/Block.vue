<template>
  <div class="block" v-if="showBolck">Click me</div>
</template>

<script>
export default {
  name: "Block",
  data() {
    return { showBolck: false };
  },
  props: ["delay"],
  mounted() {
    setTimeout(() => {
      this.showBolck = true;
    }, this.delay);
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
