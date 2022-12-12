<script>
export default {
    data() {
        return {

        }
    }
}
</script>

<template>
    <main>
        <div class="container">
            <div class="cont-footer">
                <div class="cont">

                </div>
                <div class="cont">

                </div>
                <div class="cont">

                </div>
            </div>



        </div>
    </main>

</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

main {
    height: 380px;
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-image: url("/images/footer-bg.jpg");


    .container {
        width: 60%;
        height: 100%;
        display: flex;
        justify-content: space-evenly;
        align-items: center;
        color: white;

        .cont-footer {
            width: 380px;
            height: 100%;
            display: flex;

            .cont {
                width: calc(100% / 3);
                height: 100%;
            }
        }

    }

}
</style>
