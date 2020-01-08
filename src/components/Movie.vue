<template>
    <div class="Movie">
        <img v-if="ImageLoc" alt="Avengers Poster" :src="ImageLoc"/>
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
    background-color: #2c3e50;
    color: white;
    position: relative;
    display: float;
    float: left;
    
}
img {
    max-width: 400px;
    max-height: 400px;
}
</style>