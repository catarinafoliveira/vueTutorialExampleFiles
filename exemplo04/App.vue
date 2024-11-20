<style>
.negrito {
  font-weight: bold;
}
</style>

<template>
  <p v-bind:class="{negrito: negrito}">{{ msg }}</p>
  <img v-bind:src="url" v-bind:width="largura">
</template>

<script>
export default {
  data() {
    return {
      msg: "Hello World!",
      negrito: true
    };
  }
};
</script>