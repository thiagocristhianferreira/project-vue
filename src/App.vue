<template>
  <div id="app">
    <img class="imagem" alt="Vue logo" src="./assets/logo.png">
    <Comments />
  </div>
</template>

<script>
import Comments from './components/Comments.vue'

export default {
  name: 'App',
  components: {
    Comments
  }
}
</script>

<style>
  .imagem {
    display: block;
    margin: auto;
  }
</style>
