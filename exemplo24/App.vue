<template>
  <textarea v-on:click.right="createAlert"></textarea>
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
      this.text = 'right clicked'
    }
  } 
};
</script>