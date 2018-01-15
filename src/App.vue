<template lang="pug">
  .app
    .header
      app-header
    .tabs
      app-tabs(@tabClick="tabClick")
    .content
      app-content(:section="curTab")

</template>

<script>

export default {
  components: {
    appHeader: require('./components/header'),
    appTabs: require('./components/tabs'),
    appContent: require('./components/content')
  },
  data(){
    return{
      curTab: 'TAB 1'
    }
  },
  methods: {
    tabClick(tab){
      this.curTab = tab      
    }
  }
}

</script>

<style lang="scss">
</style>
