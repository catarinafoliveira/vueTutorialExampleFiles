<template>
  <p>Menu:</p>
  <img v-bind:src="imgUrl" height="100px">
  <ul>
    <li v-for="item in menu" v-on:click="imgUrl = item.foto">
      {{ item.nome }}
    </li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      imgUrl:"https://static.vecteezy.com/system/resources/previews/043/233/749/non_2x/modern-restaurant-menu-design-concept-illustration-vector.jpg",
      menu : [
      {nome:"francesinha", foto:"https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTjPeyIPM6SEVhTsHJ1mVDay0HhAymzyn5B9g&s"},
      {nome:"moelas", foto:"https://www.unileverfoodsolutions.pt/dam/global-ufs/mcos/portugal/calcmenu/recipes/PT-recipes/In-Development/moelas/main-header.jpg"},
      {nome:"sardinhas assadas", foto:"https://www.pingodoce.pt/wp-content/uploads/2024/08/sardinhas-assadas.jpg"}
      ]
    };
  }
};
</script>