<template>
  <p>{{ "Passageiros: " + count }}</p>
  <button v-on:click="addPassageiro(1)">+1</button>
  <button v-on:click="addPassageiro(5)">+5</button>
  <button v-on:click="addPassageiro(-1)">-1</button>
</template>

<script>
export default {
  data() {
    return {
      count: 0
    }
  },
  methods: {
    addPassageiro(number) {
      this.count+=number
    }
  }
};
</script>