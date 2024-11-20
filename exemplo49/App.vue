<template>
  <h1>App.vue</h1>
  <p>The component has two &lt;div&gt; tags with one &lt;slot&gt; in each.</p>
  <slot-comp v-slot:bottomSlot>'Hello!'</slot-comp>
</template>

<style>
  #app {
    width: 300px;
  }
</style>