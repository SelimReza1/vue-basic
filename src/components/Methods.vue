<template>
  <h2>{{name}}</h2>
  <button @click="setName">Change Name</button>
  <h2>{{count}}</h2>
  <button @click="incrementCount">Increment Count</button>

  <h2>{{first}} {{last}}</h2>
  <button @click="changeHero">Change Hero</button>
</template>

<script>
import { ref, reactive, toRefs } from 'vue'
export default {
  name: 'Methods',
  setup(){
    const count=ref(0)

    const state = reactive({
      first: 'Bruce',
      last: 'Wanye',
    })
    function incrementCount(){
      count.value++
    }
    function changeHero(){
      state.first = 'Clark'
          state.last ='Kent'
    }
    return{
      count,
      incrementCount,
      ...toRefs(state),
      changeHero,

    }
  },
  data(){
    return{
      name: 'Vishwas'
    }
  },
  methods:{
    setName(){
      this.name = 'Codeacademy'
    }
  }
}
</script>

<style scoped>

</style>