<template>
  <app-header title="Upcoming movies"></app-header>
  <app-list-movies></app-list-movies>
  <app-footer></app-footer>
</template>

<script>
import AppHeader from './components/AppHeader'
import AppListMovies from "@/components/AppListMovies";
import AppFooter from "@/components/AppFooter";

export default {
  name: 'App',

  components: {
    AppFooter,
    AppListMovies,
    AppHeader
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
