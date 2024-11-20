<template>
  <div v-show="showDiv">This div tag can be hidden</div>
</template>

<script>
export default {
  data() {
    return {
      showDiv: true 
    };
  }
};
</script>