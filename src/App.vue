<template>
  <h2>{{name}}</h2>
  <button v-on:mouseover="name = 'Raz'">Change Name</button>
  <h2>{{count}}</h2>
  <button v-on:click="increment(5)">Increment</button>
  <button v-on:click="decrement(2)">Decrement</button>
</template>

<script>

export default {
  name: 'App',
  data() {
    return{
      name: 'Selim',
      count: 0,
    }
  },
  methods: {
      increment(num){
        this.count += num;
      },
      decrement(num){
        this.count -= num;
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
.underline {
  text-decoration: underline;
}
.promoted {
  font-style: italic;
}

.new {
  color: olivedrab;
}
.soldout {
  color: red;
}
</style>
