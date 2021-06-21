<template>
  <footer>
      <div class="footer_col">
          <div class="container">
                <div class="logo_footer col">
                    <img src="../assets/images/author-logo-round-200x205.png" alt="Logo footer">
                </div>
                <div class="about col">
                    <h4>About me</h4>
                    <p>Vivamus suscipit tortor eget felis porttitor volutpat. Nulla quis lorem ut libero malesuada feugiat. Vivamus suscipit tortor eget felis porttitor volupat.</p>
                </div>
                <div class="links col">
                    <h4>useful links</h4>
                    <ul>
                        <li>
                            <a href="#"> <i class="fas fa-chevron-right"></i> Latest Books</a>
                        </li>
                        <li>
                             <a href="#">Latest Books</a>
                        </li>
                        <li>
                             <a href="#">Latest Books</a>
                        </li>
                        <li>
                             <a href="#">Latest Books</a>
                        </li>
                        <li>
                             <a href="#">Latest Books</a>
                        </li>
                    </ul>
                </div>
                <div class="contact col">
                    <h4>contact info</h4>
                   <ul>
                        <li>
                            <a href="#">Latest Books</a>
                        </li>
                        <li>
                             <a href="#">Latest Books</a>
                        </li>
                        <li>
                             <a href="#">Latest Books</a>
                        </li>
                        <li>
                             <a href="#">Latest Books</a>
                        </li>
                        <li>
                             <ul class="footer_icons">
                                 <li class="icon"></li>
                                 <li class="icon"></li>
                                 <li class="icon"></li>
                                 <li class="icon"></li>
                                 <li class="icon"></li>
                             </ul>
                        </li>
                    </ul>
                </div>
          </div>
      </div>
  </footer>
</template>

<script>
export default {
    name: "Footer"

}
</script>

<style lang="scss" scoped>
    footer {
        height: 350px;
        background-image: url(../assets/images/footer-3.jpg);
        background-size: 100%;
        background-position: top;
        padding: 50px 0;

        h4 {
            color: white; 
            font-size: 16px;
            margin-bottom: 30px;
            text-transform: uppercase;
        }

        p {
            color: white; 
            font-size: 11px;
            line-height: 20px;
        }

        .container {
            display: flex;
            align-items: center;
            justify-content: space-between;

            .logo_footer img {
                height: 130px;
            }
        }

        .col {
            width: calc(100% / 4 - 40px);
            margin: 0 20px;
        }

        ul {
            list-style: none;

            li {
                font-size: 11px;

                a {
                    text-decoration: none;
                    color: white;
                }
            }
        }
    }
</style>