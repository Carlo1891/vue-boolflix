<template>
  
  <div class="top-bar">

    <h1>Boolflix</h1>

  </div>

</template>

<script>

  export default {
    name: 'Header',
    props: {
      msg: String
    }
  }

</script>


<style scoped lang="scss">

  .top-bar {
    background-color: gray;
    color: red;
  }

</style>
