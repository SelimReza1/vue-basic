<template>
  <h3>App component text</h3>
  <ChildStyles />
</template>

<script>


import ChildStyles from "./components/ChildStyles";
export default {
  name: 'App',
  components: {
    ChildStyles,
  },
  data() {
    return {
    }
  },
  methods: {

  }
}
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /*text-align: center;*/
  color: #2c3e50;
  margin-top: 60px;
}
h3{
  color: orange;
}

</style>
