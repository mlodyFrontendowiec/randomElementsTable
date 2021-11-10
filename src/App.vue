<template><Container :movies="movies" /></template>

<script>
import Container from "./components/Container/Container.vue";
export default {
  name: "App",
  components: {
    Container,
  },
  data() {
    return {
      movies: [
        { id: 1, title: "Star Wars" },
        { id: 2, title: "Indiana Jones" },
        { id: 3, title: "Jurrasic World" },
        { id: 4, title: "Skyfall" },
        { id: 5, title: "The Wolf of Wall Street" },
        { id: 6, title: "Deadpool" },
      ],
    };
  },
  methods: {
    shuffleArray() {
      this.movies = this.movies.sort(() => Math.random() - 0.5);
    },
  },
};
</script>

<style>
body {
  margin: 0;
  padding: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
}
</style>
