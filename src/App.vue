<template>
  <Card>
    <template v-slot:header>
    <h2>Header</h2>
    </template>
    <template v-slot:content>
      <h2>Content</h2>
    </template>
    <template v-slot:footer>
      <h2>Footer</h2>
    </template>
  </Card>

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
