<template>
  
  <div class="top-bar d-flex justify-content-between">

    <h1>Boolflix</h1>
    <div>

      <input type="text" placeholder="Cerca un film"  v-model="userInput">
      <button @click="$emit('choiseFilm', userInput)">Cerca</button>

    </div>

  </div>

</template>

<script>

  export default {
    name: 'Header',
    props: {
      msg: String
    },

    data (){
      return {
        userInput: "",
      }
    }
  }

</script>


<style scoped lang="scss">

  .top-bar {
    background-color: gray;
    color: red;
  }

</style>
