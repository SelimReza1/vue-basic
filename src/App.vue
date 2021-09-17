<template>
  <Card></Card>
  <Card>Card Content</Card>
  <Card><h2>Card Content Heading</h2></Card>
</template>

<script>


import Card from "./components/Card";
export default {
  name: 'App',
  components: {
    Card,
  },
  data() {
    return {
    }
  },
  methods: {

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
