<template>
  <h2>Re-usable Slot Cards</h2>
  <p>We create card-like div boxes from the foods array.</p>
  <p>We also create a card-like footer by reusing the same component.</p>
  <div id="wrapper">
    <slot-comp v-for="x in foods">
      <img v-bind:src="x.url">
      <h4>{{x.name}}</h4>
    </slot-comp>
  </div>
  <footer>
    <slot-comp>
      <h3>Footer</h3>
    </slot-comp>
  </footer>
</template>

<script>
  export default {
    data() {
      return {
        foods: [
        { name: 'Apple', desc: 'Grow on trees.'},
        { name: 'Pizza', desc: 'Very tasty'}
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