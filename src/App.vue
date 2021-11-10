<template>
  <div class="wrapper">
    <section><button @click="shuffleArray">Mix Movies</button></section>
    <Container :movies="movies" />
  </div>
</template>

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
section {
  width: 50%;
  background-color: cadetblue;
  margin: 20px auto;
  padding: 10px 0;
  box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
}
button {
  padding: 7px 14px;
  background: none;
  border: none;
  box-shadow: rgba(0, 0, 0, 0.16) 0px 0.5px 4px, rgb(0, 0, 0) 0px 0px 0px 2px;
  cursor: pointer;
  display: block;
  margin: 20px auto;
  font-size: 15px;
  color: white;
  background-color: rgb(103, 188, 190);
  transition: 0.4s;
}
button:hover {
  color: white;
  background-color: rgb(115, 206, 207);
}
</style>
