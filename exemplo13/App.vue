<template>
  <p>Menu:</p>
  <figure v-for="x in menu">
    <img v-bind:src="x.foto" width="60px">
    <figcaption>{{ x.nome }}</figcaption>
  </figure>
</template>

<script>
export default {
  data() {
    return {
      menu : [
      {nome:"francesinha", foto:"https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTjPeyIPM6SEVhTsHJ1mVDay0HhAymzyn5B9g&s"},
      {nome:"moelas", foto:"https://www.unileverfoodsolutions.pt/dam/global-ufs/mcos/portugal/calcmenu/recipes/PT-recipes/In-Development/moelas/main-header.jpg"},
      {nome:"sardinhas assadas", foto:"https://www.pingodoce.pt/wp-content/uploads/2024/08/sardinhas-assadas.jpg"}
      ]
    };
  }
};
</script>