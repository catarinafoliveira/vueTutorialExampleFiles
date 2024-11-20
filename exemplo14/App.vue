<template>
  <main>
    <p>{{ "Numero de cliques: " + count }}</p>
    <button v-on:click="count++">Contar cliques</button>
  </main>
</template>

<script>
export default {
  data() {
    return {
      count: 0 
    };
  }
};
</script>