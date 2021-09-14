<template>
<div>{{greet}} {{name}}</div>
  <div v-html="channel"></div>
  <div :id="headingId">Heading</div>
  <button :disabled="isDisabled">Bind</button>
  <h2 class="underline">underline</h2>
  <h2 class="underline" :class="status">Status</h2>
  <h2 :class="isPromoted && 'promoted'">Promoted Movie</h2>
  <h2 :class="isSoldout? 'soldout' : 'new'">Soldout? Movie</h2>
  <h2 :class="['new', 'promoted']">Newly Promoted Movie</h2>
  <h2 :class="[isPromoted && 'promoted', isSoldout? 'soldout' : 'new']">Array Conditional Movie</h2>
  <h2 :class="{
                promoted: isPromoted,
                new : !isSoldout,
                soldout: isSoldout
              }">Object Conditional Movie</h2>
  <h2 :style="{
    color: highlightColor,
    fontSize: headerSize + 'px',
    padding: '20px'
}">Inline Style</h2>
  <h2 :style="headerStyleObject">Style Object</h2>
  <h2 :style="[baseStyleObject, successStyleObject]">Success Style</h2>
  <h2 :style="[baseStyleObject, dangerStyleObject]">Danger Style</h2>
</template>

<script>

export default {
  name: 'App',
  data() {
    return{
      greet:"Hello",
      name:"Selim",
      channel:"<b>Component</b>",
      headingId: "heading",
      isDisabled: false,
      status: 'success',
      isPromoted: false,
      isSoldout: true,
      highlightColor: 'orange',
      headerSize: 50,
      headerStyleObject: {
        color: 'orange',
        fontSize: '50px',
        padding: '20px',
      },
      baseStyleObject: {
        fontSize: '50px',
        padding: '10px',
      },
      successStyleObject: {
        color: 'green',
        background: 'lightgreen',
        border: '1px solid green',
        padding: '20px',
      },
      dangerStyleObject: {
        color: 'dark',
        background: 'red',
        border: '1px solid dark',
      },
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.underline {
  text-decoration: underline;
}
.promoted {
  font-style: italic;
}

.new {
  color: olivedrab;
}
.soldout {
  color: red;
}
</style>
