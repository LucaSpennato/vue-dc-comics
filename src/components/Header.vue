<template>
  <header>
    <div class="container p-3">
      <nav class="navbar navbar-expand-lg p-0">
        <div class="row container-fluid d-flex">

          <div class="col-6 col-lg-1">
            <a href="#"><img src="../assets/img/dc-logo.png" alt="dc-logo" /></a>
          </div>

          <ul class="col-11 d-none d-lg-block text-end">
            <li v-for="(link, index) in DcComicsNavLinks" :key="index">
              <a class="py-lg-5 px-lg-2 mx-lg-1"
                :href="link.url"
                :class="{ active_el: link.isActive === true }"
                @click.prevent="navActiveOnClick(index)"
                >{{ link.text }}</a
              >
            </li>
          </ul>

          <!-- hamburger menu -->
          <div class="col-6 d-block d-lg-none text-end">
            <button class="btn btn-primary " @click="hamburgerMenu()">X</button>
          </div>
          <div class="hambuger-menu d-block d-lg-none"
          :class="{'d-none' : isHambOpen === false}">

            <div class="col-12">
              <ul class="text-center">

              <li v-for="(link, index) in DcComicsNavLinks" 
                  :key="index"
                  class="d-block p-2">

                  <a class="p-0"
                    :href="link.url"
                    :class="{ active_side_el: link.isActive === true }"
                    @click.prevent="navActiveOnClick(index)"
                    >{{ link.text }}</a>
                    
            </li>
          </ul>
            </div>
          </div>

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
      isHambOpen: false,
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
    hamburgerMenu: function(){
      this.isHambOpen = !this.isHambOpen;
    },

    navActiveOnClick: function (index) {
      this.DcComicsNavLinks.forEach((element) => {
        element.isActive = false;
      });
      console.log(index)
      this.DcComicsNavLinks[index].isActive = true;
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
      // padding: 3.2rem 0;
      // margin: 0 1rem;
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
        bottom: -2.5px;
        left: 0;
      }
      &.active_side_el::after {
        content: "\0020";
        position: absolute;
        width: 1.5rem;
        border-top: 5px solid $primaryColor;
        text-align: center;
        transform: rotate(90deg);
        bottom: 40%;
        right: 100%;
      }

      &.active_el, &.active_side_el {
        color: $primaryColor;
      }

      &:hover {
        color: $primaryColor;
      }
    }
  }
}
</style>