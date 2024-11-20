<template>
  <p>{{ msg }}</p>
  <img v-bind:src="url" width="100px">
</template>

<script>
export default {
  data() {
    return {
      msg: "Hello World!",
      url: "https://vuejsbr-docs-next.netlify.app/logo.png",
      
    };
  }
};
</script>