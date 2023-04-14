<script>
export default {
    name: "AppFooter",
    data() {
        return {
            dcComicsList: [
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
                    nameList: "Videos",
                    url: "#"
                },
                {
                    nameList: "News",
                    url: "#"
                }
            ],

            shopList: [
                {
                    nameList: "Shop DC",
                    url: "#"
                },
                {
                    nameList: "Shop DC collectibles",
                    url: "#"
                },
            ],

            dcList: [
                {
                    nameList: "Terms Of Use",
                    url: "#"
                },
                {
                    nameList: "Privacy policy (new)",
                    url: "#"
                },
                {
                    nameList: "Ad choices",
                    url: "#"
                },
                {
                    nameList: "Advertising",
                    url: "#"
                },
                {
                    nameList: "Jobs",
                    url: "#"
                },
                {
                    nameList: "Subscriptions",
                    url: "#"
                },
                {
                    nameList: "Talent Workshops",
                    url: "#"
                },
                {
                    nameList: "CPSC Certificates",
                    url: "#"
                },
                {
                    nameList: "Ratings",
                    url: "#"
                },
                {
                    nameList: "Shop Help",
                    url: "#"
                },
                {
                    nameList: "Contact Us",
                    url: "#"
                }
            ],
            sitesList: [
                {
                    nameList: "DC",
                    url: "#"
                },
                {
                    nameList: "MAD Magazine",
                    url: "#"
                },
                {
                    nameList: "DC Kids",
                    url: "#"
                },
                {
                    nameList: "DC Universe",
                    url: "#"
                },
                {
                    nameList: "DC Power Visa",
                    url: "#"
                },
            ]
        }
    }
}
</script>

<template>
    <footer>
        <div class="upper-footer">
            <div class="container">
                <div class="row">
                    <div class="col">
                        <ul>
                            <li><h3>DC Comics</h3></li>
                            <li v-for="name in dcComicsList"><a href="">{{name.nameList}}</a></li>
                        </ul>
                        <ul>
                            <li><h3>Shop</h3></li>
                            <li v-for="name in shopList"><a href="">{{name.nameList}}</a></li>
                        </ul>
                    </div>
                    <div class="col">
                        <ul>
                            <h3>DC</h3>
                            <li v-for="name in dcList"><a href="">{{name.nameList}}</a></li>
                        </ul>
                    </div>
                    <div class="col">
                        <ul>
                            <h3>Sites</h3>
                            <li v-for="name in sitesList"><a href="">{{name.nameList}}</a></li>
                        </ul>
                    </div>
                </div>
            </div>
            <img src="../assets/img/dc-logo-bg.png" alt="DC logo" class="dc-logo">
        </div>
        <div class="lower-footer">
            <div class="sign-up-btn">Sign up now!</div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use "../style/general.scss" as *;
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

.upper-footer {
    padding: 35px 0 45px 0;
    background-image: url(../assets/img/footer-bg.jpg);
    background-size: cover;
    position: relative;
    overflow: hidden;

    .row{
        @include flex(row, left, start);

        ul{
            color: white;
            padding: 0 30px 15px 0;

            h3{
                text-transform: uppercase;
                color: white;
            }

            li {
                // debug
                color: gray;
                // end debug
            }
        }
    }

    .dc-logo{
        width: 35%;
        position: absolute;
        top: -90px;
        right: 200px;
    }
}

</style>