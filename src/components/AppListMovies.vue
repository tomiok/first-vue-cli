<template>
  <p v-if="movies.length===0"> no movies to show</p>
  <template v-else>
    <p> {{ movies.length }} {{ named }} to show </p>
    <ul :class="{
           oneItem: movies.length === 1,
           multipleItems: movies.length > 1,
          }">
      <li v-for="m in movies" :key="m">{{ m }}
      </li>
    </ul>
  </template>
  <form @submit.prevent="add">
    <label> {{ form_add }}: </label>
    <input type="text" v-model="newMovie"/>
    <br>
    <button type="submit">add</button>
  </form>
  <br>
  <button @click="clear"> clear data</button>
  <br>
</template>
<script>

export default {
  name: "AppListMovies",
  data() {
    return {
      movies: [],
      named: "movies",
      form_add: "add movie",
      newMovie: ""
    }
  },
  methods: {
    clear() {
      this.movies = [];
    },
    add() {
      this.movies.push(this.newMovie);
      this.newMovie = "";
    }
  }
}
</script>

<style scoped>
ul {
  padding: 10px;
  list-style: none;
  text-align: center;
}

.oneItem {
  border: 1px solid burlywood;
}

.multipleItems {
  border: 1px solid coral;
}
</style>