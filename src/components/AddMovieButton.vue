<template>
    <button id="add-movie" @click="showModal()">Add a Movie</button>    
</template>
<script>
export default {
    methods: {
        showModal() {
            this.$emit('showModal');
        }
    }
}
</script>
<style scoped>

</style>