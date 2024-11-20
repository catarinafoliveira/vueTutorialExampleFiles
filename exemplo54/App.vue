<template>
  <h1>Example</h1>
  
  <button @click="fetchData">Fetch data</button>
  <div v-if="data" id="dataDiv">
    <img :src="data.avatar" alt="avatar">
    <pre>{{ data.first_name + " " + data.last_name }}</pre>
    <p>"{{ data.employment.title }}"</p>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        data: null,
      };
    },
    methods: {
      async fetchData() {      
        const response = await fetch("https://random-data-api.com/api/v2/users"); 
        this.data = await response.json();
      },    
    }
  };
</script>

<style>
#dataDiv {
  width: 200px;
  border: solid black 1px;
  margin-top: 10px;
  padding: 10px;
}
#dataDiv > img {
  width: 100%;
}
pre {
  font-size: larger;
  font-weight: bold;
}
</style>