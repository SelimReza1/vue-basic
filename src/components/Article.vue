<template>
  <div>
<h2>Article Component</h2>
  <h3>{{ title }}</h3>
  <h3>Likes - {{ likes }}</h3>
  <h3>Published - {{isPublished ? 'Yes' : 'No'}}</h3>
  </div>
</template>

<script>
export default {
  name: 'Article',
  props: {
    title:{
      type: String,
      required: true,
      default: 'Article Default Title'
    } ,
    likes: Number,
    isPublished: Boolean,
  },
}

</script>