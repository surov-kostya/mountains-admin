<template lang="pug">
  section.blog
    .blog__title Страница "Блог"
    .blog__subtitle Добавить запись
    input(type="text" placeholder="Название")
    input(type="text" placeholder="Дата")
    textarea(placeholder="Содержание")
    button(type="button") Добавить
</template>
<style lang="scss" src="styles/blog.scss" scoped>

</style>
<script>
export default {
  
}
</script>
