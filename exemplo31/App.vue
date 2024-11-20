<template>
  <p> Important item? <input type="checkbox" v-model="important"> {{ isImportant }} </p>
</template>

<script>
export default {
  data() {
    return {
      important: false 
    }
  },
  computed: {
    isImportant() {
      if(this.important){
        return 'yes'
      }
      else {
        return 'no'
      }
    }
  } 
};
</script>