<template>
  <p>Menu:</p>
  <img v-for="x in fotosMenu" v-bind:src="x" width="100px">
</template>

<script>
export default {
  data() {
    return {
      fotosMenu : [
      "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTjPeyIPM6SEVhTsHJ1mVDay0HhAymzyn5B9g&s",
      "https://www.unileverfoodsolutions.pt/dam/global-ufs/mcos/portugal/calcmenu/recipes/PT-recipes/In-Development/moelas/main-header.jpg",
      "https://www.pingodoce.pt/wp-content/uploads/2024/08/sardinhas-assadas.jpg"
      ]
    };
  }
};
</script>