<template>
  <p>Move the mouse pointer over the box below:</p>
  <div v-on:mousemove="mousePos" style="background-color: grey;">
    <span>xPos: {{ xPos }}</span><br>
    <span>yPos: {{ yPos }}</span>
  </div>
</template>

<script>
export default {
  data() {
    return {
      xPos: 0,
      yPos: 0
    }
  },
  methods: {
    mousePos(event) {
      this.xPos = event.offsetX
      this.yPos = event.offsetY
    }
  }
};
</script>