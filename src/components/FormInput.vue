<template>
  <div class="form-todo form-group">
      <p>
        <input placeholder="nome" type="text" name="author" class="form-control" v-model="name" />
      </p>
      <p>
        <textarea placeholder="Comentário" name="message"  class="form-control" v-model="message" />
      </p>
      <button v-on:click="addComment" type="submit" class="btn btn-primary">Comentar</button>
    </div>
</template>

<script>
export default {
  data() {
    return {
      name: '',
      message: ''
    }
  },
  methods: {
    addComment() {
      if (this.message.trim() === '') {
        return false;
      }
  
      this.$emit('add-comment', {
        name: this.name,
        message: this.message,
      });
  
      this.name = '';
      this.message = '';
    },
  }
}
</script>
