<script>
export default {
  data() {
    return {
      links: [
        {
          name: "CHARACTERS",
          href: "#",
          attributeType: false
        },
        {
          name: "COMICS",
          href: "#",
          attributeType: true
        },
        {
          name: "MOVIES",
          href: "#",
          attributeType: false
        },
        {
          name: "TV",
          href: "#",
          attributeType: false
        },
        {
          name: "GAMES",
          href: "#",
          attributeType: false
        },
        {
          name: "COLLECTIBLES",
          href: "#",
          attributeType: false
        },
        {
          name: "VIDEOS",
          href: "#",
          attributeType: false
        },
        {
          name: "FANS",
          href: "#",
          attributeType: false
        },
        {
          name: "NEWS",
          href: "#",
          attributeType: false
        },
        {
          name: "SHOP",
          href: "#",
          attributeType: false
        },
      ]

    }
  }
}
</script>

<template>
  <header>
    <div class="cont-header">
      <div>
        <img src="/images/dc-logo.png" class="img-header">
      </div>

      <ul>
        <li v-for="(item, index) in links" :key="index" class="list-header">
          <a :href="item.href" :class="{ active: item.attributeType }">
            {{ item.name }}
          </a>

        </li>
      </ul>

    </div>

  </header>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

header {

  // height: 120px;
  padding: 20px;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;

  .cont-header {
    max-width: 1200px;
    width: 60%;
    height: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    // background-color: aquamarine;
  }

  .img-header {
    width: 80px;
    height: 80px;
  }

  ul {
    display: flex;

    li {
      margin-right: 20px;
      list-style-type: none;

      a {
        text-decoration: none;
        color: black;
        font-size: 13px;


        &.active,
        &:hover {
          color: $color-type;
          height: 1px;
          position: relative;
          width: 40%;
          border-bottom: 4px solid $color-type;
        }

      }

    }

  }



}
</style>
