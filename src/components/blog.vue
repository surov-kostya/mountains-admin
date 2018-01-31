<template lang="pug">
  section.blog
    .blog__title Страница "Блог"
    form.blog__form(method='POST', action='/article')
      .blog__subtitle Добавить запись
      input(type="text" name="title" placeholder="Название")
      input(type="text" name="date" placeholder="Дата")
      textarea(name="body" placeholder="Содержание")
      button(type="submit") Добавить
</template>
<style lang="scss" src="styles/blog.scss" scoped>

</style>
<script>
export default {
  
}
</script>
