<script>
export default {
    data() {
        return {
            dcComics:
                [
                    {
                        name: "Characters",
                        href: "#"
                    },
                    {
                        name: "Comics",
                        href: "#"
                    },
                    {
                        name: "Movies",
                        href: "#"
                    },
                    {
                        name: "TV",
                        href: "#"
                    },
                    {
                        name: "Games",
                        href: "#"
                    },
                    {
                        name: "Videos",
                        href: "#"
                    },
                    {
                        name: "News",
                        href: "#"
                    },

                ],
            dc: [
                {
                    name: "Terms Of Use",
                    href: "#"
                },
                {
                    name: "Privacy policy (New)",
                    href: "#"
                },
                {
                    name: "Ad Choices",
                    href: "#"
                },
                {
                    name: "Advertising",
                    href: "#"
                },
                {
                    name: "Jobs",
                    href: "#"
                },
                {
                    name: "Subscriptions",
                    href: "#"
                },
                {
                    name: "Talent WOrkshops",
                    href: "#"
                },
                {
                    name: "CPSC Certificates",
                    href: "#"
                },
                {
                    name: "Ratings",
                    href: "#"
                },
                {
                    name: "Shop Help",
                    href: "#"
                },
                {
                    name: "Contact Us",
                    href: "#"
                },

            ],
            sites: [
                {
                    name: "DC",
                    href: "#"
                },
                {
                    name: "MAD Magazine",
                    href: "#"
                },
                {
                    name: "DC Kids",
                    href: "#"
                },
                {
                    name: "DC Universe",
                    href: "#"
                },
                {
                    name: "DC Power Visa",
                    href: "#"
                },
            ],
            shop: [
                {
                    name: "Shop DC",
                    href: "#"
                },
                {
                    name: "Shop DC Collectibles",
                    href: "#"
                },
            ],

        }
    }
}
</script>

<template>
    <main>
        <div class="container">
            <div class="cont-footer">
                <div class="cont">
                    <ul>
                        <li class="title">
                            <strong class="font-title">DC COMICS</strong>
                        </li>
                        <li class="sub" v-for="(item, index) in dcComics" :key="index">
                            <a :href="item.href">{{ item.name }} </a>

                        </li>
                    </ul>
                </div>
                <div class="cont">
                    <ul>
                        <li class="title">
                            <strong class="font-title">DC</strong>
                        </li>
                        <li class="sub" v-for="(item, index) in dc" :key="index">
                            <a :href="item.href">{{ item.name }} </a>

                        </li>
                    </ul>
                </div>
                <div class="cont">
                    <ul>
                        <li class="title">
                            <strong class="font-title">SITES</strong>
                        </li>
                        <li class="sub" v-for="(item, index) in sites" :key="index">
                            <a :href="item.href">{{ item.name }} </a>

                        </li>
                    </ul>
                </div>
                <div class="cont height">
                    <ul class="shop">
                        <li class="title ">
                            <strong class="font-title">SHOP</strong>
                        </li>
                        <li class="sub" v-for="(item, index) in shop" :key="index">
                            <a :href="item.href">{{ item.name }} </a>

                        </li>
                    </ul>
                </div>
                <!-- <div class="cont height">
                    <ul class="shop">
                        <li class="title ">
                            <strong class="font-title">SHOP</strong>
                        </li>
                        <li class="sub" v-for="(item, index) in arrayFooter" :key="index">
                            <strong class="font-title">{{item.title}}</strong>
                            <a :href="item.href">{{ item.name }} </a>

                        </li>
                    </ul>
                </div> -->


            </div>

            <img src="/images/dc-logo-bg.png" class="img">

        </div>
    </main>

</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

main {
    // height: 500px;
    padding: 60px;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    background-image: url("/images/footer-bg.jpg");

    .container {
        max-width: 1200px;
        width: 70%;
        height: 100%;
        display: flex;
        align-items: center;
        color: white;
        position: relative;

        .cont-footer {
            //  width: 450px;
            height: 100%;
            display: flex;
            flex-wrap: wrap;

            .cont {
                width: calc(100% / 3);

                li {
                    line-height: 21px;
                    list-style-type: none;

                    a {
                        text-decoration: none;
                        color: #6c6d6f;

                    }

                    .font-title {
                        font-size: 18px;

                    }
                }

                .shop {
                    margin-top: -50px;

                }


            }

        }

        .title {
            color: white;
            font-weight: bold;
            margin-bottom: 6px;


        }


        .img {
            // width: 550px;
            // height: 550px;
            position: absolute;
            right: 0;
            z-index: 10;
            // filter: invert(48%) sepia(5%) saturate(174%) hue-rotate(182deg) brightness(85%) contrast(84%);
        }

    }

}
</style>
