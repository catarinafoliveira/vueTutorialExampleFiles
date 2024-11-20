<template>
  <button v-on:click.once="writeText">Click me!</button>
  <div> {{ text }} </div>
</template>

<script>
export default {
  data() {
    return {
      text: 'not clicked '
    }
  },
  methods: {
    writeText() {
      this.text += 'clicked'
    }
  } 
};
</script>