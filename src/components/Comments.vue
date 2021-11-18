<template>
  <div class="container">
    <h1>Comentários</h1>
    <hr />
    <div class="form-todo form-group">
      <p>
        <input placeholder="nome" type="text" name="author" class="form-control" />
      </p>
      <p>
        <textarea placeholder="Comentário" name="message"  class="form-control"></textarea>
      </p>
      <button type="submit" class="btn btn-primary">Comentar</button>
    </div>
    <div class="list-group">
      <div class="list-group-item">
        <span class="comment__author">Autor: <strong>Primeiro autor</strong></span>
        <p>Primeiro Comentário</p>
        <div>
          <a href="#" title="Excluir">Excluir</a>
        </div>
      </div>
    </div>
    <hr />
  </div>
</template>

<script>
export default {
  data() {
    return {
      comments: [],
      name: '',
      message: '',
    }
  }
}
</script>

