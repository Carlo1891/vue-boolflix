<template>
  
  <div class="main-content">
    <h2 class="text-white">Films</h2>
  </div>

</template>

<script>

  import axios from "axios";

  export default {
    name: 'Main',
    data (){
      return {
        userInput: "",
        apiUrl: "https://api.themoviedb.org/3/movie/550?api_key=082c0ba1f05244482622e8fa6699b301",
        listMovie: []
      }
    },

    created (){
      this.formMovie()
    },
    
    methods: {
      formMovie (){
        axios
        .get(this.apiUrl)
        .then ((result) => {
          this.listMovie = result.data.results
          console.log (result);
        })
      }
    }
  }

</script>


<style scoped lang="scss">

  .main-content {
    background-color: black;
    height: 100vh;
  }

</style>
