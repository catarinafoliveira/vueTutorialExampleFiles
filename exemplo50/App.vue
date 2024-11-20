<template>
  <h1>Local Component</h1>
  <p>App.vue controls how local data from the scoped slot is rendered.</p>
  <slot-comp v-slot="dataFromSlot">
    <h2>{{ dataFromSlot.lclData }}</h2>
  </slot-comp>
</template>

<style>
#app {
  width: 300px;
}
h2 {
  padding: 10px;
}
</style>   