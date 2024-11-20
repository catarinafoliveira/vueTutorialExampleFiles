<style>
.impClass {
  font-weight: bold;
}
#ulFound li {
  text-decoration: line-through;
}
</style>

<template>
  <form v-on:submit.prevent="addItem">
    <p>Add item</p>
    <p>Item name: <input type="text" required v-model="itemName"></p>
    <p>How many: <input type="number" v-model="itemNumber"></p>
    <p> Important? <input type="checkbox" v-model="important"> {{ important }} </p>
    <button type="submit">Add item</button>
  </form>
  <div>
    <p><strong>Shopping list:</strong></p>
    <ul id="ulToFind">
      <li 
        v-for="item in shoppingList" 
        v-bind:class="{ impClass: item.important }"
        v-on:click="item.found=!item.found"
        v-show="!item.found">
        {{ item.name }}, {{ item.number}}
      </li>
    </ul>
    <br>
    <ul id="ulFound">
      <li 
        v-for="item in shoppingList" 
        v-bind:class="{ impClass: item.important }"
        v-on:click="item.found=!item.found"
        v-show="item.found">
        {{ item.name }}, {{ item.number}}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      itemName: null,
      itemNumber: null,
      important: false,
      shoppingList: [
      { name: 'Tomatoes', number: 5, important: false, found: false },
      { name: 'Bread', number: 1, important: false, found: false }
      ]
    }
  },
  methods: {
    addItem(){
      let item = {
        name: this.itemName,
        number: this.itemNumber,
        important: this.important,
        found: false
      }
      this.shoppingList.push(item)
      this.itemName = null
      this.itemNumber = null  
      this.important = false
    }
  }
};
</script>