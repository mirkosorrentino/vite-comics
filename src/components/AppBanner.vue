<script>
export default {
    name: "AppBanner",
    data() {
        return {
            
        }
    }
}
</script>

<template>
    <div class="banners">
        <div class="container">
            <ul>
                <li>
                    <img src="../assets/img/buy-comics-digital-comics.png" alt="">
                    <div>Digital comics</div>
                </li>
                <li>
                    <img src="../assets/img/buy-comics-merchandise.png" alt="">
                    <div>DC merchandise</div>
                </li>
                <li>
                    <img src="../assets/img/buy-comics-subscriptions.png" alt="">
                    <div>subscription</div>
                </li>
                <li>
                    <img src="../assets/img/buy-comics-shop-locator.png" alt="">
                    <div>Comic shop locator</div>
                </li>
                <li>
                    <img src="../assets/img/buy-dc-power-visa.svg" alt="">
                    <div>DC power visa</div>
                </li>
            </ul>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../style/general.scss" as *;
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

.banners {
    width: 100%;
    padding: 30px 0;
    background-color: $banners-color;

    ul{
        @include flex(row, space-around, center);
        font-size: .9rem;
        
        li{
            text-transform: uppercase;
            color: white;
            @include flex(row, left, center);
            
            img{
                width: 20%;
                padding-right: 10px;
            }
        }
    }
}

</style>