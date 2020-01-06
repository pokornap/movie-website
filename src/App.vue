<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <div v-for="(movie, index) in movies" :key="index">
      <Movie
      :MovieTitle="movie.title"
      :MovieDescription="movie.description"
      :ImageLoc="movie.image"
    />
    </div>
    
  </div>
</template>

<script>
import Movie from "./components/Movie.vue";
export default {
  name: "app",
  data: () => ({
      movies: [
        {
          title: "Avengers: Endgame",
          description: "This is an amazing movie, go watch it!",
          image: "AvengersEndgame.png"
        },
        {
          title: "Star Wars",
          description: "The OG Star Wars",
          image: "StarWars.png"
        },
        {
          title: "Atomic Blonde",
          description: "The CIA always wins",
          image: "AtomicBlonde.png"
        }
      ]
  }),
  components: {
    Movie
  }
};
</script>

<style>
html body {
  background-color: #2c3e50;
}
#app {
  font-family: "Lucida Console", Monaco, monospace;
  font-size: 16px;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;
}
</style>
