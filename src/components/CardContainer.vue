<script>
export default {
    props: {
        cards: Array,
    },
    data() {
        return {

        }
    }
}
</script>

<template>
    <ul>

        <li v-for="(card, index) in cards" :key="index">
            <a href="">
                <img :src="card.thumb" alt="">
                <div class="text">{{ card.series }}</div>
            </a>
        </li>

    </ul>
    <div class="cont-btn">
        <a href="" class="btn">LOAD MORE</a>
    </div>

</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

ul {
    display: flex;
    flex-wrap: wrap;

    li {
        list-style-type: none;
        width: calc(100% / 6);
        height: 200px;
        margin-bottom: 50px;

        .text {
            font-size: 17px;
            width: 180px;
        }

        img {
            height: 160px;
            width: 160px;
        }

    }
}

a {
    text-decoration: none;
    color: white;
}

.cont-btn {
    height: 60px;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;

    .btn {
        padding: 10px 50px;
        background-color: $color-type;
        color: white;
        font-size: 15px;
    }

}
</style>
