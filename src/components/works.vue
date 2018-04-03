<template lang="pug">
  .works
    h2.works__header Мои работы
    form.works__form(enctype="multipart/form-data" method="post")  
      .works__title Добавить работу
      label.works__label
        span.works__span Заголовок
        input.works__input(type='text' name='work-name' placeholder="Введите заголовок" required)
      label.works__label
        span.works__span Список технологий     
        input.works__input(type='text' name='work-date' placeholder="Используемые технологии")
      label.works__label
        span.works__span Ссылка на проект     
        input.works__input(type='text' name='work-link' placeholder="Ссылка")
      label.works__label
        span.works__span Прикрепить картинку
        input.works__load(type="file")
      button.works__add(type="submit" @click="addWork") Добавить проект      
</template>

<script>
export default {
  methods: {
    addWork() {
      console.log('work was added');
    }
  }
};
</script>