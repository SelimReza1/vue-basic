<template>
<h2 v-for="(name, index) in names" :key="name">{{ index }}{{ name }}</h2>
  <h2 v-for="name in fullnames" :key="name.first">{{name.first}} {{name.last}}</h2>

  <div v-for="actor in actors" :key="actor">
    <h2>{{ actor.name }}</h2>
    <h3 v-for="movie in actor.movies" :key="movie">{{ movie }}</h3>
  </div>

  <h2 v-for="(value, key, index) in myInfo" :key="value">{{ index }} {{ key }} {{ value }}</h2>
</template>

<script>

export default {
  name: 'App',
  data() {
    return{
    names : ['Selim', 'Aftab', 'Kajal'],
      fullnames: [
        {first: 'Selim', last:'Reza'},
        {first: 'Aftab', last:'Ahmed'},
        {first: 'Kajal', last:'afrin'},
      ],
      actors: [
        {
          name: 'chirstian Bale',
          movies: ['Batman', 'The Prestige'],
        },
        {
          name: 'Di Caprio',
          movies: ['Titanic', 'Inception'],
        }
      ],
      myInfo: {
        name: 'Selim',
        email: 'selimreza9920@gmail.com',
        course: 'Software Engineering',
      }
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
