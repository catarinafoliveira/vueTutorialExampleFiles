<style>
.impClass {
  font-weight: bold;
}
</style>

<template>
  <form v-on:submit.prevent="addItem">
    <p>Add item</p>
    <p>Item name: <input type="text" required v-model="itemName"></p>
    <p>How many: <input type="number" v-model="itemNumber"></p>
    <p> Important? <input type="checkbox" v-model="important"> {{ important }}    </p>
    <button type="submit">Add item</button>
  </form>
  <hr>
  <p>Shopping list:</p>
  <ul>
    <li v-for="item in shoppingList" v-bind:class="{ impClass: item.important }">{{item.name}}, {{item.number}}</li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      itemName: null,
      itemNumber: null,
      important: false,
      shoppingList: [
      { name: 'Tomatoes', number: 5, important: false }
      ]
    }
  },
  methods : {
    addItem(){
      let item = {
        name: this.itemName,
        number: this.itemNumber,
        important: this.important
      }
      this.shoppingList.push(item)
      this.itemName = null
      this.itemNumber = null  
      this.important = false
    }
  }
};
</script>