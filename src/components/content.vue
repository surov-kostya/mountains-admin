<template lang="pug">
  main
    app-about(v-if="section === 'TAB 1'")
    app-blog(v-else-if="section === 'TAB 2'")
    app-works(v-else-if="section === 'TAB 3'")
</template>
<style lang="scss" src="styles/content.scss">
</style>



<script>

export default {
  components: {
    appAbout: require('./about'),
    appBlog: require('./blog'),
    appWorks: require('./works')
  },
  props: {
    section: ''
  }
}

</script>