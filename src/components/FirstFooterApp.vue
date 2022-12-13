<script>
export default {
    data() {
        return {
            dcComics:
                [
                    {
                        title: "DC COMICS",
                        list: [
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

                    },
                ],

            dc: [
                {

                    title: "DC",
                    list: [


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
                    ]
                }
            ],
            sites: [
                {
                    title: "SITES",
                    list: [

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
                    ]
                }
            ],
            shop:
                [
                    {

                        title: "SHOP",
                        list: [

                            {
                                name: "Shop DC",
                                href: "#"
                            },
                            {
                                name: "Shop DC Collectibles",
                                href: "#"
                            },
                        ]
                    }
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
                        <li class="sub" v-for="(item, index) in dcComics" :key="index">
                            <a href="" class="title-text ">{{ item.title }}</a>
                            <a :href="item.href" v-for="(items, index) in item.list">{{ items.name }} </a>

                        </li>
                    </ul>
                </div>
                <div class="cont">
                    <ul>
                        <li class="sub" v-for="(item, index) in dc" :key="index">
                            <a href="" class="title-text ">{{ item.title }}</a>
                            <a :href="item.href" v-for="(items, index) in item.list">{{ items.name }} </a>

                        </li>
                    </ul>
                </div>
                <div class="cont">
                    <ul>
                        <li class="sub" v-for="(item, index) in sites" :key="index">
                            <a href="" class="title-text ">{{ item.title }}</a>
                            <a :href="item.href" v-for="(items, index) in item.list">{{ items.name }} </a>

                        </li>
                    </ul>
                </div>
                <div class="cont height">
                    <ul>
                        <li class="sub" v-for="(item, index) in shop" :key="index">
                            <a href="" class="title-text ">{{ item.title }}</a>
                            <a :href="item.href" v-for="(items, index) in item.list">{{ items.name }} </a>

                        </li>
                    </ul>
                </div>

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

                    list-style-type: none;

                    a {
                        line-height: 21px;
                        display: block;
                        text-decoration: none;
                        color: #6c6d6f;

                    }

                    .title-text {
                        color: white;
                        font-weight: bold;
                        margin-bottom: 6px;
                    }


                }

                .shop {
                    margin-top: -50px;

                }


            }

            .height {
                margin-top: -60px;

            }

        }


        .img {

            position: absolute;
            right: 0;
            z-index: 10;

        }

    }

}
</style>
