<template>
  <h3>Slots Fallback Content</h3>
  <p>A component without content provided can have fallback content in the slot tag.</p>
  <slot-comp>
    <!-- Empty -->
  </slot-comp>
  <slot-comp>
    <h4>This content is provided from App.vue</h4>
  </slot-comp>
</template>

<style>
  #app div {
    width: 150px;
  }
  h4 {
    text-align: center;
  }
</style>