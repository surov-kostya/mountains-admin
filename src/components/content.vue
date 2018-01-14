<template lang="pug">
  main
    app-about
    app-blog
    app-works
</template>
<style lang="scss" src="styles/content.scss">
</style>



<script>

export default {
  components: {
    appAbout: require('./about'),
    appBlog: require('./blog'),
    appWorks: require('./works')
  }
}

</script>