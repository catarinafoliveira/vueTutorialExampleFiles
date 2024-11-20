<template>
  <p v-bind:style="estilo">{{ msg }}</p>
  <img v-bind:src="url" v-bind:width="largura">
</template>

<script>
export default {
  data() {
    return {
      msg: "Hello World!",
      url: "https://vuejsbr-docs-next.netlify.app/logo.png",
      largura: "200px",
      estilo: "color:blue;"
    };
  }
};
</script>