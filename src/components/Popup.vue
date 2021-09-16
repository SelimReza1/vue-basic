<template>
<h2>This is a popup</h2>
  <input type="text" v-model="name">
  <button @click="$emit('close', name)">Close popup</button>
</template>

<script>
export default {
  name: 'Popup',
  emits: {
    close: (name) => {
    if(!name){
      return false
    } else {
      return true
    }
    }
  },
  data(){
    return {
      name: ''
    }
  }
}
</script>

<style scoped>

</style>