<template>
  <p v-if="movies.length===0"> no movies to show</p>
  <template v-else>
    <p> {{ movies.length }} {{ named }} to show </p>
    <ul :class="{
           oneItem: movies.length === 0,
           multipleItems: movies.length > 1,
          }">
      <li v-for="m in movies" :key="m">{{ m }}
      </li>
    </ul>
  </template>
</template>

<script>

export default {
  name: "AppListMovies",
  data() {
    return {
      movies: ["Batman I", "Spider man", "Dune", "House of Gucci"],
      named: "movies"
    }

  },
}
</script>

<style scoped>
ul {
  padding: 10px;
  list-style: none;
  text-align: justify;
}
.oneItem {
  border: 1px solid burlywood;
}

.multipleItems {
  border: 1px solid coral;
}
</style>