<template>
    <div class="TopBar">
        <h1>This is the nav bar</h1>
        <AddMovieModal></AddMovieModal>
    </div>    
</template>

<script >
import AddMovieModal from "./AddMovieModal.vue";
export default {
    name: "TopBar",
    props: {},
    components: {
        AddMovieModal
    }
}
</script>

<style scoped>

.TopBar {
    height: 75px;
    float: both;
    clear: both;
    padding-top: 5px;
    padding-left: 15px;
    color: white;
    background-color: #2c2c50;
    text-align: left;    
}




</style>