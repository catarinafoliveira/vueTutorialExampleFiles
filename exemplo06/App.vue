<template>
  <p v-if="condicao">
    in stock
  </p>
  <p v-else>
    not in stock
  </p>
</template>

<script>
export default {
  data() {
    return {
      condicao: true
    };
  }
};
</script>