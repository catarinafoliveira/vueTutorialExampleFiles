<template>
  Important item?
  <input type="checkbox" v-model="important"> {{ important }}
</template>

<script>
export default {
  data() {
    return {
      important: false 
    }
  }
};
</script>