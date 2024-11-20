<template>
  <p v-if="menu.includes('sardinhas')">The menu includes sardinhas</p>
  <p v-else-if="menu.includes('francesinha')">The menu includes francesinha, but not sardinhas</p>
  <p v-else>The menu does not include francesinha or sardinhas</p>
</template>

<script>
export default {
  data() {
    return {
      menu: "O menu de hoje inclui: francesinha, moelas e sardinhas assadas." 
    };
  }
};
</script>