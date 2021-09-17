<template>
<h3 v-for="name in names" :key="name.firstname">
  <slot :firstname = "name.firstname" :lastname="name.lastname"></slot>
</h3>
</template>

<script>
export default {
  name: 'NameList',
  data(){
    return {
      names: [
        {
          firstname: 'Selim',
          lastname: 'Hossain',
        },
        {
          firstname: 'Kabita',
          lastname: 'Hossain',
        },
        {
          firstname: 'Mou',
          lastname: 'Akter',
        }
      ]
    }
  }
}
</script>

<style scoped>

</style>