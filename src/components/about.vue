<template lang="pug">
  section.about
    .about__title Страница "Обо мне"
    .about__skills.skill
      ul.skill__list
        li.skill__item(v-for="skillItem in skillList")
          table.table
            tr.table__header
              th.table__title {{skillItem}}
            tr.table__data(v-for="tech in skills")
              td.table__technology {{tech}}
              td.table__input
                input(type="text").table_percent
              td.table__sign %
      button(type="button") Сохранить
</template>

<style lang="scss" src="styles/about.scss">
</style>


<script>
export default {
  data() {
    return{
      skillList: ['frontend', 'backend', 'workflow'],
      skills: []
    }
  },
  created() {
    fetch("./data.json")
      .then(response => {
        return response.json();
      })
      .then(data => {
        this.skills = data;
      });
  }
}
</script>
