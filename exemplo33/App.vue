<style>
div {
  border-style: solid;
  height: 50px;
}
</style>

<template>
  <div v-on:click="updatePos"></div>
  <p><code>{{xPos}} ({{ xDiff }})</code></p>
</template>

<script>
export default {
  data() {
    return {
      xPos: 0,
      xDiff: 0
    }
  },
  watch: {
    xPos(newVal,oldVal) {
      this.xDiff = newVal-oldVal
    }
  },
  methods: {
    updatePos(evt) {
      this.xPos = evt.offsetX
    }
  }
};
</script>