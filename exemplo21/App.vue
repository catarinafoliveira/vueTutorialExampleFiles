<template>
  <input v-on:keydown="getKey">
  <p> {{ keyValue }} </p>
</template>

<script>
export default {
  data() {
    return {
      keyValue: ''
    }
  },
  methods: {
    getKey(evt) {
      this.keyValue = evt.key
    }
  } 
};
</script>