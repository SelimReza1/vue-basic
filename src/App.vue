<template>
<ComponentC />
  <h2>AppComponent Username {{ name }}</h2>
</template>

<script>


import ComponentC from "./components/ComponentC";
export default {
  name: 'App',
  components: {
    ComponentC

  },
  data(){
    return{
    name: 'Selim'
    }
  },
  provide() {
    return{
      username: this.name
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
