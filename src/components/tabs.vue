<template lang="pug">
  ul.tabs__list
    li.tabs__item(v-for='tab in tabs')
      a.tabs__btn(href="#" @click="tabClick") {{tab}}
</template>

<style lang="scss" src="styles/tabs.scss">
</style>

<script>
export default {
  data() {
    return {
      tabs: ['TAB 1', 'TAB 2', 'TAB 3', 'TAB 4']
    }
  },
  methods:{
    tabClick: function (e){
      this.$emit('tabClick', e.currentTarget.innerText)
    }
  }
}
</script>

