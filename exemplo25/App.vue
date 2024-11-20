<template>
  <textarea v-on:click.left.ctrl="createAlert"></textarea>
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
      this.text = 'left clicked while holding ctrl'
    }
  } 
};
</script>