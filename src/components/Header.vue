<template>
  <header>
    <nav class="navbar navbar-expand-lg p-0">
      <div class="container-fluid d-flex align-items-center">
            
        <a href="#"><img src="../assets/img/dc-logo.png" alt="dc-logo"/></a>

        <ul>
            <li 
            v-for="(link, index) in DcComicsNavLinks"
            :key="index">
                <a :href="link.url" >{{ link.text }}</a>
            </li>
        </ul>


      </div>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Header",
  data(){
        return{
            DcComicsNavLinks: [
                {
                    text: 'characters',
                    url: '#',
                },
                {
                    text: 'comics',
                    url: '#',
                },
                {
                    text: 'movies',
                    url: '#',
                },
                {
                    text: 'tv',
                    url: '#',
                },
                {
                    text: 'games',
                    url: '#',
                },
                {
                    text: 'collectibles',
                    url: '#',
                },
                {
                    text: 'videos',
                    url: '#',
                },
                {
                    text: 'fans',
                    url: '#',
                },
                {
                    text: 'news',
                    url: '#',
                },
                {
                    text: 'shop',
                    url: '#',
                },
            ],
        };
    },
    methods: {
        // TODO aggiungi prevent al click
        // TODO crea un hamb menu magari
    },
};
</script>

<style lang="scss">
@import "../styles/variables.scss";

header{
    img {
    width: 4.5rem;
    }
    ul{
        list-style: none;

        li{
            display: inline-block;
            position: relative;
        }
        a{
            color: black;
            padding: 3.2rem 0;
            margin: 0 1rem;
            text-transform: uppercase;
            text-decoration: none;
            position: relative;
            font-weight: 500;
            font-size: .8rem;
            line-height: 120%;

            &.active_el::after{
                content: '\0020';
                position: absolute;
                width: 100%;
                border-top: 5px solid $primaryTextColor;
                text-align: center;
                bottom: 0;
                left: 0;
            }

            &.active_el{
                color: $primaryTextColor;
            }
            
            &:hover{
                color: $primaryTextColor;
            }
        }
    }
}
</style>