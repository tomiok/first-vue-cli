<template>
  <h1> {{ title }}</h1>
</template>

<script>
  export default {
    name: "AppHeader",
    props: ["title"]
  }
</script>

<style>
h1 {
  text-align: center;
  text-decoration: underline;
}
</style>