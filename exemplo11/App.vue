<template>
  <p>Menu:</p>
  <p v-for="(x, index) in itemsMenu">
    {{ index + 1}}: {{ x }} <br>
  </p>
</template>

<script>
export default {
  data() {
    return {
      itemsMenu : [
      "francesinha",
      "moelas",
      "sardinhas assadas"
      ]
    };
  }
};
</script>