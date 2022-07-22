<template>

    <div id="app">

        <Header @choiseMovie="changeMovie"/>
        <Main :titleMovie="titleMovie"/>

    </div>

</template>

<script>

    import Header from "./components/Header.vue";
    import Main from "./components/Main.vue";

    export default {
        name: 'App',
        components: {
            Header,
            Main
        },

        data (){
            return {
                titleMovie: ""
            }
        },
        
        methods: {
            changeMovie (movie){
                this.titleMovie= movie;
            }
        }
    }

</script>

<style lang="scss">

    @import "~bootstrap/dist/css/bootstrap.css";
    
</style>
