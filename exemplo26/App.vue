<template>
  <div v-on:click.right.prevent="changeColor" v-bind:style="{ backgroundColor:'hsl('+bgColor+',80%,80%)' }">
    Right click me
  </div>
</template>

<script>
export default {
  data() {
    return {
      bgColor : 0
    }
  },
  methods: {
    changeColor() {
      this.bgColor+=100;
    }
  }
};
</script>