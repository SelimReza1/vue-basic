<template>
<h2>This is a popup</h2>
  <button @click="$emit('close', 'Selim')">Close popup</button>
</template>

<script>
export default {
  name: 'Popup',
  emits: ['close'],
}
</script>

<style scoped>

</style>