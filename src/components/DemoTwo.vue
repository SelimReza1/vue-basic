<template>
<div>
  <h2>{{firstName}}  {{lastName}}</h2>

  <h2>{{faname}} {{lname}}</h2>
</div>
</template>

<script>
import {reactive, toRefs} from "vue";

export default {
  name: 'DemoTwo',
  setup(){
    const state = reactive({
      firstName: 'Bruce',
      lastName: 'Waynwe',
    })
    setTimeout(()=>{
      state.firstName = 'Clacrk'
          state.lastName = 'Kent'
      console.log(state)
    }, 2000)
  return toRefs(state)
  },
  data(){
    return{
      faname: 'Bruce',
      lname: 'Wayne',
    }
  },
}
</script>

<style scoped>

</style>