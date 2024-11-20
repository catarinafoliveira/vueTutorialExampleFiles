<template>
  <div id="adultos">
    Adultos:
    <button v-on:click="addAnimal($event,1)">+1</button>
    <button v-on:click="addAnimal($event,5)">+5</button>
    <button v-on:click="addAnimal($event,-1)">-1</button>
  </div>
  <div id="criancas">
    Criancas:
    <button v-on:click="addAnimal($event,1)">+1</button>
    <button v-on:click="addAnimal($event,5)">+5</button>
    <button v-on:click="addAnimal($event,-1)">-1</button>
  </div>
  <ul>
    <li>Adultos: {{ adultos }}</li>
    <li>Criancas: {{ criancas }}</li>
    <li>(Total: {{ adultos + criancas }})</li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      adultos: 0,
      criancas: 0
    }
  },
  methods: {
    addAnimal(e,number) {
      if(e.target.parentElement.id==="adultos"){
        this.adultos+=number;
      }
      else if(e.target.parentElement.id==="criancas"){
        this.criancas+=number;
      }
    }
  }
};
</script>