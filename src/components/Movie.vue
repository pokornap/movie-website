<template>
    <div class="Movie">
        <img alt="Avengers Poster" :src="require(`@/assets/${ImageLoc}`)"/>
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
    background-color: blue;
    position: relative;
    display: float;
    float: left;
    
}
img {
    max-width: 400px;
    max-height: 400px;
}
</style>