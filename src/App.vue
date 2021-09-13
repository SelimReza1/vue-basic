<template>
<div>{{greet}} {{name}}</div>
  <div v-html="channel"></div>
  <div v-bind:id="headingId">Heading</div>
  <button v-bind:disabled="isDisabled">Bind</button>
</template>

<script>

export default {
  name: 'App',
  data() {
    return{
      greet:"Hello",
      name:"Selim",
      channel:"<b>Component</b>",
      headingId: "heading",
      isDisabled: false,
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
