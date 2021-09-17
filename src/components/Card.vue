<template>
<div class="card"><slot>Default Content</slot></div>
</template>

<Script>
export default {
  name: 'Card',
}
</Script>

<style scoped>
.card{
  box-shadow: 0px 4px 8px 0px #f2f2f2;
  transition: .3s;
  padding: 20px;
  width: 200px;
  margin-bottom: 20px;
}
.card:hover{
  box-shadow: 0px 8px 16px 0px #f2f2f2;
}
</style>