<template>
  <h2>Hello {{ name }} Hero {{ heroName }}</h2>
</template>

<script>
export default {
  name: 'Greet',
  props: ['name', 'heroName']
}
</script>