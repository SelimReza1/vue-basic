<template>
  <input type="text" :value="modelValue" @input="$emit('update:modelValue', $event.target.value)" />
</template>

<script>
export default {
  name: 'Input',
  props: {
    modelValue: String,
  }
}
</script>

<style scoped>

</style>