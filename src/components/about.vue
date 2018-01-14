<template lang="pug">
  section.about
    .about__title Страница "Обо мне"
    .about__skills.skill
      ul.skill__list
        li.skill__item(v-for="skillItem in skillList")
          table.table
            tr.table__header
              th.table__title {{skillItem}}
            tr.table__data(v-for="tech in skills" v-if="checkSkillItem(skillItem) ===  tech.type")
              td.table__technology {{tech.name}}
              td.table__input
                input(type="text" :value="tech.percents").table_percent
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
  methods:{
    checkSkillItem(skillItem){
      switch(skillItem) {
        case 'frontend' : return 1;
        case 'backend' : return 2;
        case 'workflow' : return 3;
      }
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
