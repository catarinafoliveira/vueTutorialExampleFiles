<template>
  <h3>Slots in Vue</h3>
  <p>We create card-like div boxes from the foods array.</p>
  <div id="wrapper">
    <slot-comp v-for="x in foods">
      <h4>{{x.name}}</h4>
      <p>{{x.desc}}</p>
    </slot-comp>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        foods: [
        { name: 'Apple', desc: 'Grow on trees.'},
        { name: 'Pizza', desc: 'Very tasty'},
        { name: 'Rice', desc: 'Grain food.'},
        { name: 'Fish', desc: 'Lives in water.'}
      ]
      }
    }
  }
</script>

<style>
  #wrapper {
    display: flex;
    flex-wrap: wrap;
  }
</style>