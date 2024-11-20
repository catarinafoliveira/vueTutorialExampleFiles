<template>
  <textarea v-on:keydown.ctrl.s="createAlert"></textarea>
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
    createAlert() {
      this.text = 'pressed ctrl + s'
    }
  } 
};
</script>