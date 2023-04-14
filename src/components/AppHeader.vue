<script>
export default {
    name: "AppHeader",
    data() {
        return {
            navList: [
                {
                    nameList: "Characters",
                    url: "#"
                },
                {
                    nameList: "Comics",
                    url: "#"
                },
                {
                    nameList: "Movies",
                    url: "#"
                },
                {
                    nameList: "TV",
                    url: "#"
                },
                {
                    nameList: "Games",
                    url: "#"
                },
                {
                    nameList: "Collectibles",
                    url: "#"
                },
                {
                    nameList: "Videos",
                    url: "#"
                },
                {
                    nameList: "Fans",
                    url: "#"
                },
                {
                    nameList: "News",
                    url: "#"
                },
                {
                    nameList: "Shop",
                    url: "#"
                },
            ]
        }
    }
}
</script>

<template>
  <header>
    <div class="container">
        <div class="header-content">
            <div class="logo">
                <a href=""><img src="../assets/img/dc-logo.png" alt="DC Comics logo"></a>
            </div>
            <div class="nav-bar">
                <ul>
                    <li v-for="name in navList"><a href="">{{name.nameList}}</a></li>
                </ul>
            </div>
        </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;
@use "../style/general.scss" as *;

header{
    background-color: $header-color;

.header-content{
    @include flex(row, space-between, center);
    padding: 10px;
    
    
    .logo img {
        width: 70%;
    }

    ul {
        display: flex;

        a {
            text-decoration: none;
            color: inherit;
        }

        li {
            text-transform: uppercase;
            padding-right: 1.5rem;
        }
    }
}
}
</style>