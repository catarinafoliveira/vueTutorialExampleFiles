<template>
  <input type="text" v-model="inpText">
  <p> {{ inpText }} </p>
</template>

<script>
export default {
  data() {
    return {
      inpText: 'Initial text' 
    }
  }
};
</script>