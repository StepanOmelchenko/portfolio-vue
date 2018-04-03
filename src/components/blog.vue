<template lang="pug">
  .blog
    h2.blog__header Мой блог
    .blog__title Добавить статью
    form.blog__form
      label.blog__label
        span.blog__span Заголовок статьи
        input(type='text' name='article-name' class='blog__input' placeholder="Заголовок" required)
      label.blog__label
        span.blog__span Дата публикации
        input(type='text' name='article-date' class='blog__input' placeholder="Дата" required)  
      label.blog__label      
        textarea(type="text" name='article-text' class='blog__textarea' placeholder="Текст статьи")   
      button.blog__btn(type="button" @click="addArticle") Добавить статью    
</template>
<script>
  export default {
  methods: {
    addArticle() {
      console.log('article was added');
    }
  }
  };
</script>