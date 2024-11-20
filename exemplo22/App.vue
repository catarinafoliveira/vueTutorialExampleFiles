<template>
  <main>
    <textarea v-on:keyup.s="createAlert"></textarea>
    <div> {{ text }} </div>
  </main>
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
      this.text = 'pressed s'
    }
  } 
};
</script>