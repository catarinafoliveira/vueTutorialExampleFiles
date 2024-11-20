<style>
.negrito {
  font-weight: bold;
}
.italico {
  font-style: italic;
}
</style>

<template>
  <p v-bind:class="{negrito: negrito, italico: italico}">{{ msg }}</p>
  <img v-bind:src="url" v-bind:width="largura">
</template>

<script>
export default {
  data() {
    return {
      msg: "Hello World!",
      negrito: true,
      italico:true
    };
  }
};
</script>