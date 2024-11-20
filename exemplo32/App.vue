<template>
  <input type="range" min="0" max="100" step="1" v-model="rangeVal">
  <p><code>{{ rangeVal }}</code></p> 
</template>

<script>
export default {
  data() {
    return {
      rangeVal: 50
    }
  },
  watch: {
    rangeVal(val) {
      if( val>20 && val<60 ){
        if(val<40){
          this.rangeVal = 20;
        }
        else{
          this.rangeVal = 60;
        }
      }
    }
  }
};
</script>