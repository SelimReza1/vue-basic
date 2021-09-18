<template>
  <input type="text" placeholder="First Name" v-model="firstName" />
  <input type="text" placeholder="last Name" v-model="lastName" />
  <h2>Full Name is: {{fullName}}</h2>

  <input type="text" placeholder="First Name" v-model="refFirstName" />
  <input type="text" placeholder="Last Name" v-model="refLastName" />
  <h2>Composition Full Name is: {{refFullName}}</h2>

  <input type="text" placeholder="First Name" v-model="reactiveFirstName" />
  <input type="text" placeholder="Last Name" v-model="reactiveLastName" />
  <h2>Reactive Full Name is: {{ reactiveFullName }}</h2>

</template>

<script>
import { ref, computed, reactive, toRefs } from 'vue'
export default {
  name:'Computed',
  setup(){
      const refFirstName = ref('')
      const refLastName =ref('')
    const refFullName = computed(function () {
      return refFirstName.value+' '+refLastName.value
    })

    const state = reactive({
      reactiveFirstName: '',
      reactiveLastName: '',
    })
    const reactiveFullName = computed(function (){
      return state.reactiveFirstName+ ' '+state.reactiveLastName
    })
        return{
          refFirstName,
          refLastName,
          refFullName,
          ...toRefs(state),
          reactiveFullName,
        }
  },

  data(){
    return{
      firstName: '',
      lastName: ''
    }
  },
  computed:{
    fullName(){
      return this.firstName+' '+this.lastName
    }
  }
}
</script>

<style scoped>

</style>