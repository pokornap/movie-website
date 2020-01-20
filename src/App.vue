<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <!-- <Movie
      MovieTitle="Avengers: Endgame"
      MovieDescription="This is an amazing movie, go watch it!"
      ImageLoc="AvengersEndgame.png"
    />-->
    <div>
      <Nav>

      </Nav>
    </div>
    <div v-for="(movie, index) in movies" :key="index">
      <Movie
        :MovieTitle="movie.name"
        :MovieDescription="movie.description"
        :ImageLoc="movie.imageUrl"
      />
    </div>
  </div>
</template>

<script>
import Nav from "./components/Nav.vue";
import Movie from "./components/Movie.vue";
import axios from "axios";
export default {
  name: "app",
  data: () => ({
    movies: []
  }),
  components: {
    Movie,
    Nav
  },
  mounted: function() {
    setTimeout(async()=>{
      var res = await axios.get("https://api.forcemx.com/colts/movie");
      if(res.data.length > 0){
        res.data.forEach(element => {
          console.log(element);
          this.$data.movies.push(element);
        });
      }
    });  
  },
  // methods: {
  //   new_movie: function(movieName, MovieDescription, ImageLink) {
  //     console.log(movieName);
  //   }
  // }
};

</script>

<style>
html body {
  background-color: #57557c;
}
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