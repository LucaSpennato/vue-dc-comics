<template>
  <header>
    <nav class="navbar navbar-expand-lg p-0">
      <div class="container-fluid d-flex align-items-center">
            
        <div class="p-3">
            <a href="#"><img src="../assets/img/dc-logo.png" alt="dc-logo"/></a>
        </div>

        <ul>
            <li>
                <a class="active_el" href="#">characters</a>
            </li>
            <li>
                <a href="#">comics</a>
            </li>
            <li>
                <a href="#">movies</a>
            </li>
            <li>
                <a href="#">tv</a>
            </li>
            <li>
                <a href="#">games</a>
            </li>
            <li>
                <a href="#">collectibles</a>
            </li>
            <li>
                <a href="#">videos</a>
            </li>
            <li>
                <a href="#">fans</a>
            </li>
            <li>
                <a href="#">news</a>
            </li>
            <li>
                <a href="#">shop</a>
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
// height: 6rem;
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
                border-top: 5px solid $HeaderTextColor;
                // background-color: $mainTextColor;
                text-align: center;
                bottom: 0;
                left: 0;
            }

            &.active_el{
                color: $HeaderTextColor;
            }
            
            &:hover{
                color: $HeaderTextColor;
            }
        }
    }
}
</style>