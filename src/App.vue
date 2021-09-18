<template>
  <ClickCounter />
  <hover-counter />
</template>

<script>
import ClickCounter from "./components/ClickCounter";
import HoverCounter from "./components/HoverCounter";
export default {
  name: 'App',
  components: {
    HoverCounter,
    ClickCounter,

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
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

</style>
