<template>
  <button v-on:click="writeText">Click me!</button>
  <div> {{ text }} </div>
</template>

<script>
export default {
  data() {
    return {
      text: ''
    }
  },
  methods: {
    writeText() {
      this.text = 'Hello World!'
    }
  } 
};
</script>