<script>
export default {
    name: "AppHeader",
    data() {
        return {
            
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
                    <a href=""><li>Characters</li></a>
                    <a href=""><li>Comics</li></a>
                    <a href=""><li>Movies</li></a>
                    <a href=""><li>Tv</li></a>
                    <a href=""><li>Games</li></a>
                    <a href=""><li>Collectibles</li></a>
                    <a href=""><li>Videos</li></a>
                    <a href=""><li>Fans</li></a>
                    <a href=""><li>News</li></a>
                    <a href=""><li>Shop</li></a>
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