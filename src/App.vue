<template>
<!--<Greet name="Vaijan" heroName="Salman" />-->
<!--<Greet name="3 Idiot" heroName="Amir"/>-->
<!--<Greet name="Happy New Year" heroName="SRK" />-->
<!--  <Greet :name="name" :heroName="heroName" />-->
  <Article title="Article Title" :likes="50" :is-published="true" />
</template>

<script>

//import Greet from "./components/Greet";
import Article from "./components/Article";
export default {
  name: 'App',
  components: {
  //  Greet,
    Article,
  },
  data(){
    return{
      name: 'Dhoom 2',
      heroName: 'Hrittik',
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /*text-align: center;*/
  color: #2c3e50;
  margin-top: 60px;
}


</style>
