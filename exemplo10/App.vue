<template>
  <p>Menu:</p>
  <ul>
    <li v-for="x in itemsMenu">{{ x }}</li>
  </ul>
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