<template>
{{2+4+4}}
  <h2>Add Method - {{ add(2,3,6) }}</h2>
  <h2>Multiply Method - {{multiply(basevalue)}}</h2>
</template>

<script>

export default {
  name: 'App',
  data() {
    return{
    basemultiplier: 5,
      basevalue: 2,
    }
  },
  methods: {
      add(a,b,c){
        return a+b+c;
      },
    multiply(num)  {
        return num * this.basemultiplier;
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
