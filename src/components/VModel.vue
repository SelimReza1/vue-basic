<template>
  <input type="text" placeholder="FirstName" v-model="fName" />
  <input type="text" placeholder="lastName" v-model="lName" />

  <input type="text" placeholder="Hero name" v-model="heroName" />
  <input type="text" placeholder="FirstName" v-model="firstName" />
  <input type="text" placeholder="lastName" v-model="lastName" />
</template>

<script>
import {ref, reactive, toRefs} from 'vue'
export default {
name:'VModel',
  setup(){
  const heroName = ref()
  const state = reactive({
        firstName: '',
        lastName: '',
    })
    return{
    heroName,
      ...toRefs(state),

    }
  },

  data (){
  return {
    fName: '',
    lName: '',
  }
  }
}
</script>

<style scoped>

</style>