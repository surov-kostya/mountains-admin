<template lang="pug">
  .app
    .header
      app-header
    .tabs
      app-tabs
    .content
      app-content

</template>

<script>

export default {
  components: {
    appHeader: require('./components/header'),
    appTabs: require('./components/tabs'),
    appContent: require('./components/content')
  }
}

</script>

<style lang="scss">
</style>
