<template>
  <header class="py-3">
    <nav class="navbar navbar-expand-lg">
      <div class="container-fluid">
            
        <a href="#"><img src="../assets/img/dc-logo.png" alt=""/></a>

        <ul>
            <li>
                <a class="active_el" href="#">Home</a>
            </li>
            <li>
                <a href="#">Home</a>
            </li>
            <li>
                <a href="#">Home</a>
            </li>
            <li>
                <a href="#">Home</a>
            </li>
            <li>
                <a href="#">Home</a>
            </li>
            <li>
                <a href="#">Home</a>
            </li>
            
        </ul>


      </div>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style lang="scss" scoped>
@import "~bootstrap/scss/bootstrap.scss";

    img {
    width: 4rem;
    }
    ul{
        list-style: none;

        li{
            display: inline;
        }
        a{
            color: black;
            padding: 2rem 0;
            margin: 0 1rem;
            text-decoration: none;
            position: relative;

            &.active_el{
                color: blue;
            }
            &.active_el::after{
                content: '\0020';
                position: absolute;
                width: 100%;
                border: 3px solid red;
                background-color: red;
                text-align: center;
                bottom: 0;
                left: 0;
            }
            &:hover{
                color: orange;
            }
        }
    }

</style>