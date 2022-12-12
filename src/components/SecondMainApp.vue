<script>
export default {
    data() {
        return {
            obj: [
                {
                    img: "/images/buy-comics-digital-comics.png",
                    href: "#",
                    name: "DIGITAL COMICS"
                },
                {
                    img: "/images/buy-comics-merchandise.png",
                    href: "#",
                    name: "DC MERCHANDISE"
                },
                {
                    img: "/images/buy-comics-subscriptions.png",
                    href: "#",
                    name: "SUBSCRIPTION"
                },
                {
                    img: "/images/buy-comics-shop-locator.png",
                    href: "#",
                    name: "COMIC SHOP LOCATOR"
                },
                {
                    img: "/images/buy-dc-power-visa.svg",
                    href: "#",
                    name: "DC POWER VISA"
                },
            ]


        }
    }
}
</script>

<template>
    <main>
        <div class="container">
            <ul>
                <li v-for="(item, index) in obj" :key="index">
                    <img :src="item.img" class="img">
                    <a :href="item.href">
                        {{ item.name }}
                    </a>
                </li>
            </ul>
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

main {
    height: 150px;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: $color-type;
    position: relative;
    z-index: 50;


    .container {
        width: 60%;
        height: 100%;
        display: flex;
        justify-content: space-between;
        align-items: center;
        color: white;

        ul {

            display: flex;

            li {
                margin-right: 40px;
                list-style-type: none;

                a {
                    text-decoration: none;
                    color: white;
                    font-size: 15px;
                    margin-left: 10px;
                }

                .img {
                    height: 55px;
                    width: 46px;
                    vertical-align: middle;
                }


            }
        }
    }

}
</style>
