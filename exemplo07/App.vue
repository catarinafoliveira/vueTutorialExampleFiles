<template>
  <p v-if="quantidade>3">
    in stock
  </p>
  <p v-else-if="quantidade>0">
    limited
  </p>
  <p v-else>
    not in stock
  </p>
</template>

<script>
export default {
  data() {
    return {
      quantidade: 3
    };
  }
};
</script>