<template>
  <section>
    <MovieItem v-for="movie in movies" :movie="movie" :key="movie.id" />
  </section>
</template>

<script>
import MovieItem from "../MovieItem/MovieItem.vue";
export default {
  name: "Container",
  components: {
    MovieItem,
  },
  props: { movies: Array },
};
</script>

<style scoped>
section {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
  background-color: cadetblue;
  box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
  width: 50vw;
  margin: 10vh auto;
  padding: 50px;
}
</style>
