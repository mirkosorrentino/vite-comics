<script>
export default {
    name: "AppJumbotron",
}
</script>

<template>
    <div class="jumbotron">
        <img src="../assets/img/jumbotron.jpg" alt="DC jumbotron">
    </div>
</template>

<style lang="scss" scoped>
// @use "../style/partials/variables" as *;

.jumbotron{
    height: 300px;
    
    img {
        width: 100%;
    }
}
</style>