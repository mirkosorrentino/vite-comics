<script>
export default {
    name: "AppComic",
    props: {
        image: String,
        title: String,
        type: String
    }
}
</script>

<template>
    <div class="card">
        <img :src="image" :alt="type">
        <div class="comic-title">{{ title }}</div>
    </div>
</template>

<style lang="scss" scoped>
// @use "../style/partials/variables" as *;
 .card {
    width: calc(100% / 6 - 10px);
    margin: 5px;
    padding: 0 5px;

    img {
        max-width: 100%;
        width: 170px;
        height: 170px;
        padding-top: 10px;
    }

    .comic-title {
        color: white;
        text-transform: uppercase;
        font-size: .7rem;
        padding-top: 10px;
    }
}
</style>