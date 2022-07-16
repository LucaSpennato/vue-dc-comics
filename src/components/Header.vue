<template>
  <header>
    <div class="container p-3">
      <nav class="navbar navbar-expand-lg p-0">
        <div class="container-fluid d-flex align-items-center">
          <a href="#"><img src="../assets/img/dc-logo.png" alt="dc-logo" /></a>

          <ul>
            <li v-for="(link, index) in DcComicsNavLinks" :key="index">
              <a
                :href="link.url"
                :class="{ active_el: link.isActive === true }"
                @click.prevent="navActiveOnClick(index)"
                >{{ link.text }}</a
              >
            </li>
          </ul>
        </div>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      DcComicsNavLinks: [
        {
          text: "characters",
          url: "#",
          isActive: true,
        },
        {
          text: "comics",
          url: "#",
          isActive: false,
        },
        {
          text: "movies",
          url: "#",
          isActive: false,
        },
        {
          text: "tv",
          url: "#",
          isActive: false,
        },
        {
          text: "games",
          url: "#",
          isActive: false,
        },
        {
          text: "collectibles",
          url: "#",
          isActive: false,
        },
        {
          text: "videos",
          url: "#",
          isActive: false,
        },
        {
          text: "fans",
          url: "#",
          isActive: false,
        },
        {
          text: "news",
          url: "#",
          isActive: false,
        },
        {
          text: "shop",
          url: "#",
          isActive: false,
        },
      ],
    };
  },
  methods: {
    // TODO crea un hamb menu magari
    navActiveOnClick: function (index) {
      this.DcComicsNavLinks.forEach((element) => {
        element.isActive = false;
      });
      if (this.DcComicsNavLinks[index].isActive === false) {
        this.DcComicsNavLinks[index].isActive = true;
      }
    },
  },
};
</script>

<style lang="scss">
@import "../styles/variables.scss";

header {
  img {
    width: 4.5rem;
  }
  ul {
    list-style: none;

    li {
      display: inline-block;
      position: relative;
    }
    a {
      color: black;
      padding: 3.2rem 0;
      margin: 0 1rem;
      text-transform: uppercase;
      text-decoration: none;
      position: relative;
      font-weight: 500;
      font-size: 0.8rem;
      line-height: 120%;

      &.active_el::after {
        content: "\0020";
        position: absolute;
        width: 100%;
        border-top: 5px solid $primaryColor;
        text-align: center;
        bottom: 0;
        left: 0;
      }

      &.active_el {
        color: $primaryColor;
      }

      &:hover {
        color: $primaryColor;
      }
    }
  }
}
</style>