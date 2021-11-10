<template>ok</template>

<script>
export default {
  name: "App",

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
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
}
</style>
