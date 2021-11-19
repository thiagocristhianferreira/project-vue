<template>
  <div class="list-group">
    <div class="list-group-item" v-for="(comment, index) in allComments" v-bind:key="index">
      <span class="comment__author">Autor: <strong>{{ comment.name }}</strong></span>
      <p>{{ comment.message }}</p>
      <div>
        <a href="#" title="Excluir" v-on:click.prevent="removeComment(index)">Excluir</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    commentsArray: Array,
  },
  methods: {
    removeComment(index) {
      this.commentsArray.splice(index, 1);
    }
  },
  computed: {
    allComments() {
      return this.commentsArray.map(comment => ({
        ...comment,
        name: comment.name.trim() === '' ? 'Anonymous' : comment.name
      }))
    }
  },
  watch: {
    comments(val) {
      console.log('val', val)
    }
  }
}
</script>