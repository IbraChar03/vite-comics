<script>
export default {
    data() {
        return {
            imgSocial: [
                {
                    name: "Facebook",
                    img: "/images/footer-facebook.png"
                },
                {
                    name: "Twitter",
                    img: "/images/footer-twitter.png"
                },
                {
                    name: "Youtube",
                    img: "/images/footer-youtube.png"
                },
                {
                    name: "Pinterest",
                    img: "/images/footer-pinterest.png"
                },
                {
                    name: "Periscope",
                    img: "/images/footer-periscope.png"
                },
            ]

        }
    }
}
</script>

<template>
    <main>
        <div class="container">
            <a href="">SIGN-UP NOW!</a>
            <div>
                <strong class="text-follow">FOLLOW US</strong>
                <img class="social-img" :src="item.img" alt="" v-for="(item, index) in imgSocial" :key="index">

            </div>
        </div>
    </main>

</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

main {
    height: 130px;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #303030;
    position: relative;
    z-index: 50;


    .container {
        width: 60%;
        height: 100%;
        display: flex;
        justify-content: space-between;
        align-items: center;
        color: white;

        a {
            text-decoration: none;
            color: white;
            font-weight: bold;
            font-size: 18px;
            border: 2px solid $color-type;
            padding: 18px;

        }

        .text-follow {
            color: $color-type;
            font-size: 20px;
            margin-right: 20px;
        }

        .social-img {
            margin-right: 20px;
            vertical-align: middle;
            margin-bottom: 10px;
        }
    }

}
</style>
