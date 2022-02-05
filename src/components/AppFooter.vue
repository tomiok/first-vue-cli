<template>
  <a :href="uriLink" target="_blank"> {{ uriNamed }} </a>
</template>

<script>
export default {
  name: "AppFooter",
  data() {
    return {
      uriLink: "https://imdb.com",
      uriNamed: "checkout in IMDB"
    }
  }
}
</script>

<style scoped>

</style>