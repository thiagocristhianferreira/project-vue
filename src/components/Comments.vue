<template>
  <div class="container">
    <h1>Comentários</h1>
    <hr />
    <FormInput v-on:add-comment="addComment" />
    <CommentsList :commentsArray="comments" />
    <hr />
  </div>
</template>

<script>
import FormInput from './FormInput';
import CommentsList from './CommentsList';

export default {
  components: {
    FormInput,
    CommentsList,
  },
  data() {
    return {
      comments: []
    }
  },
  methods: {
    addComment(comment) {
      this.comments.push(comment);
    },

    removeComment(index) {
      this.comments.splice(index, 1);
    }
  },
}
</script>

