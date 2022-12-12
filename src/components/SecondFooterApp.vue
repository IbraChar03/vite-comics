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


    .container {
        width: 60%;
        height: 100%;
        display: flex;
        justify-content: space-evenly;
        align-items: center;
        color: white;

    }

}
</style>
