<template>
  <div>
    <p>{{ movie.title }}</p>
  </div>
</template>

<script>
export default {
  name: "MovieItem",
  props: {
    movie: Object,
  },
};
</script>

<style scoped>
div {
  width: 30%;
  margin-bottom: 15px;
  box-shadow: rgba(0, 0, 0, 0.16) 0px 0.5px 4px, rgb(0, 0, 0) 0px 0px 0px 2px;
  background-color: rgb(103, 188, 190);
}
p {
  color: white;
  text-align: center;
}
</style>
