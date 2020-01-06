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
    background-color: #2c2c50;
    color: white;
    position: relative;
    display: float;
    float: left;
    border-radius: 25px;
    margin: 10px
}
img {
    max-width: 400px;
    /* min-width: 400px; */
    max-height: 400px;
    /* min-height: 400px; */
}
</style>