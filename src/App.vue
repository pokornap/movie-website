<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <Movie MovieTitle="Avengers: Endgame" MovieDescription="This is an amazing movie, go watch it!" ImageLoc="AvengersEndgame.png"/>
    <Movie v-for="movie in movies" MovieTitle=`${movie.title}`/>
  </div>
</template>

<script>
import Movie from './components/Movie.vue'
export default {
  name: 'app',
  data: () => {
    movies: [
      {title: "Avengers: Endgame", description: "This is an amazing movie, go watch it!", image: "logo.png"},
      {title: "Star Wars", description: "The OG Star Wars", image: "logo.png"},
      {title: "Atomic Blonde", description: "The CIA always wins", image: "logo.png"}
    ]
  },
  components: {
    Movie
  }
}
</script>

<style>
#app {
  font-family: "Lucida Console", Monaco, monospace;
  font-size: 16px;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
