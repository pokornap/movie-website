<template>
    <div class="Movie">
        <div id="movie-bg">
            <img v-if="ImageLoc" alt="Movie Poster" :src="ImageLoc"/>
        </div>
        <h1>{{MovieTitle}}</h1>
        <p class="description">
            {{MovieDescription}}
        </p>
    </div>
</template>

<script>
export default {
    name: "Movie",
    props: {
        MovieTitle: String,
        MovieDescription: String,
        ImageLoc: String
    }
}
</script>

<style scoped>
.Movie {
    background-color: #2c2c50;
    color: white;
    position: relative;
    display: float;
    float: left;
    max-width: 400px;
    margin: 8px;
    border-radius: 10px;
}
#movie-bg {
    background-color: white;
    width: 400px;
    max-height: 400px;
    border-top-left-radius: inherit;
    border-top-right-radius: inherit;
}
img {
    max-width: 400px;
    max-height: 400px;
    
}
</style>