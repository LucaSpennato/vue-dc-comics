<template>
  <footer>
    <div class="container-fluid p-0 bg-footer-img">
      <section>
        <div class="container">
          <div class="row">
            <div class="row col-6 p-4">
              <div class="col-4 p-0">
                <ul>
                  <h5>dc comics</h5>
                  <li>
                    <a href="#">characters</a>
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

                <ul>
                  <h5>shop</h5>
                  <li>
                    <a href="#">Shop DC</a>
                  </li>
                  <li>
                    <a href="#">Shop DC Collectibles</a>
                  </li>
                </ul>
              </div>

              <div class="col-4 p-0">
                <ul>
                  <h5>dc</h5>

                  <li>
                    <a href="#">termsasdasdasdasdasasdsa</a>
                  </li>

                  <li>
                    <a href="#">termsasdasdasdasdasasdsa</a>
                  </li>
                  <li>
                    <a href="#">termsasdasdasdasdasasdsa</a>
                  </li>
                  <li>
                    <a href="#">termsasdasdasdasdasasdsa</a>
                  </li>
                  <li>
                    <a href="#">termsasdasdasdasdasasdsa</a>
                  </li>
                  <li>
                    <a href="#">termsasdasdasdasdasasdsa</a>
                  </li>
                  <li>
                    <a href="#">termsasdasdasdasdasasdsa</a>
                  </li>
                  <li>
                    <a href="#">termsasdasdasdasdasasdsa</a>
                  </li>
                  <li>
                    <a href="#">termsasdasdasdasdasasdsa</a>
                  </li>
                  <li>
                    <a href="#">termsasdasdasdasdasasdsa</a>
                  </li>
                  <li>
                    <a href="#">termsasdasdasdasdasasdsa</a>
                  </li>
                </ul>
              </div>

              <div class="col-4 p-0">
                <ul>
                  <h5>sites</h5>

                  <li>
                    <a href="#">termsasdasdasdasdasasdsa</a>
                  </li>

                  <li>
                    <a href="#">termsasdasdasdasdasasdsa</a>
                  </li>
                  <li>
                    <a href="#">termsasdasdasdasdasasdsa</a>
                  </li>
                  <li>
                    <a href="#">termsasdasdasdasdasasdsa</a>
                  </li>
                  <li>
                    <a href="#">termsasdasdasdasdasasdsa</a>
                  </li>
                  <li>
                    <a href="#">termsasdasdasdasdasasdsa</a>
                  </li>
                  <li>
                    <a href="#">termsasdasdasdasdasasdsa</a>
                  </li>
                  <li>
                    <a href="#">termsasdasdasdasdasasdsa</a>
                  </li>
                  <li>
                    <a href="#">termsasdasdasdasdasasdsa</a>
                  </li>
                  <li>
                    <a href="#">termsasdasdasdasdasasdsa</a>
                  </li>
                  <li>
                    <a href="#">termsasdasdasdasdasasdsa</a>
                  </li>
                </ul>
              </div>
            </div>
            <div class="col-6 bg-logo"></div>
          </div>
        </div>
      </section>
    </div>

    <section class="bottom-section">
      <div class="container-fluid p-0 bg-dark">
        <div class="container">
          <div class="row p-4 justify-content-between">
            <div class="col-2">
              <button class="btn btn-outline-primary text-light">
                SIGN-UP NOW!
              </button>
            </div>
            <div class="col-4">
              <h5>follow us</h5>
              <div class="icon-wrapper">
                <a href="#"
                  ><img src="../assets/img/footer-facebook.png" alt=""
                /></a>
                <a href="#"
                  ><img src="../assets/img/footer-twitter.png" alt=""
                /></a>
                <a href="#"
                  ><img src="../assets/img/footer-youtube.png" alt=""
                /></a>
                <a href="#"
                  ><img src="../assets/img/footer-pinterest.png" alt=""
                /></a>
                <a href="#"
                  ><img src="../assets/img/footer-periscope.png" alt=""
                /></a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </footer>
</template>

<script>
export default {
  name: "FooterContent",
};
</script>

<style lang="scss">
@import "../styles/variables.scss";

.bg-footer-img {
  background-image: url(../assets/img/footer-bg.jpg);
  background-repeat: no-repeat;
  background-size: cover;
}
footer {
  h5 {
    color: white;
    text-transform: uppercase;
  }
  ul {
    padding: 0;
    list-style: none;
  }
  li {
    line-height: 100%;
  }
  li a {
    text-decoration: none;
    color: gray;
    font-size: 0.7rem;
  }

  section .bg-logo {
    background-image: url(../assets/img/dc-logo-bg.png);
    background-position: center;
    background-repeat: no-repeat;
  }
  .bottom-section {
    h5 {
      color: $primaryTextColor;
      display: inline-block;
      margin-right: .3rem;
    }

    .icon-wrapper{
        display: inline-block;
        
        a{
            padding: 0 .5rem;
        }
    }
  }
}
</style>