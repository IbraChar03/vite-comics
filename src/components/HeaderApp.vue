<script>
export default {
  data() {
    return {
      active: 0,
      links: [
        {
          name: "CHARACTERS",
          href: "#",
        },
        {
          name: "COMICS",
          href: "#",
        },
        {
          name: "MOVIES",
          href: "#",
        },
        {
          name: "TV",
          href: "#",
        },
        {
          name: "GAMES",
          href: "#",
        },
        {
          name: "COLLECTIBLES",
          href: "#",
        },
        {
          name: "VIDEOS",
          href: "#",
        },
        {
          name: "FANS",
          href: "#",
        },
        {
          name: "NEWS",
          href: "#",
        },
        {
          name: "SHOP",
          href: "#",
        },
      ]

    }
  },
  methods: {
    activeLink(index) {
      this.active = index
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
        <!-- :class="{ active: item.attributeType }" -->
        <li v-for="(item, index) in links" :key="index" class="list-header">
          <a :href="item.href" :class="(active === index) ? `active` : ``" @click="activeLink(index)">
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
  padding: 10px;
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
        font-weight: bold;


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
