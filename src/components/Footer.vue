<template>
    <footer>
        <!-- Footer-top -->
        <div class="footer_col">
            <div class="container">
                <div class="logo_footer col">
                    <img src="../assets/images/author-logo-round-200x205.png" alt="Logo footer">
                </div>
                <div class="about col">
                    <h4 id="about_me">About me</h4>
                    <p>Vivamus suscipit tortor eget felis porttitor volutpat. Nulla quis lorem ut libero malesuada feugiat. Vivamus suscipit tortor eget felis porttitor volutpat.</p>
                </div>
                <div class="links col">
                    <h4>useful links</h4>
                    <ul>
                        <li v-for="(footerLink, index) in footerLinks"
                            :key="index">
                            <a href="#"> <i class="fas fa-chevron-right"></i> {{ footerLink }}</a>
                        </li>
                    </ul>
                </div>
                <div class="contact col">
                    <h4 id="contact_info">contact info</h4>
                    <ul>
                        <li v-for="(footerContact, index) in footerContacts"
                        :key="index">
                            <a href="#">{{ footerContact }}</a>
                        </li>
                        <li>
                            <ul class="footer_icons">
                                <li v-for="(footerIcon, index) in footerIcons"
                                :key="index" class="icon">
                                    <a href="#"><i :class="footerIcon"></i></a>
                                </li>
                            </ul>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
        <!-- /Footer-top -->
        <!-- Copyright -->
        <div class="footer_bottom">
            <p>© Copyright 2012 - 2021 | Avada Theme by <strong>ThemeFusion</strong> | All Rights Reserved | Powered by <strong>WordPress</strong> </p>
        </div>
        <!-- /Copyright -->
    </footer>
</template>

<script>
export default {
    name: "Footer",
    props: {
        footerLinks: Array,
        footerContacts: Array,
        footerIcons: Array
    },

}
</script>

<style lang="scss" scoped>
    footer {
        background-image: url(../assets/images/footer-3.jpg);
        background-size: 100%;
        background-position: top;
        padding: 40px 0;

        h4 {
            color: white; 
            font-size: 16px;
            margin-bottom: 20px;
            text-transform: uppercase;
        }

        #about_me {
            margin-bottom: 40px;
        }
        #contact_info {
            margin-top: 40px;
        }

        p {
            color: white; 
            font-size: 11px;
            line-height: 25px;
        }

        .links .fas {
            margin-right: 10px;
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
        }

        ul {
            list-style: none;

            li {
                font-size: 11px;

                a {
                    text-decoration: none;
                    color: white;
                    line-height: 25px;

                    &:hover {
                        color: #3da698;
                    }
                }
            }
        }

        .footer_icons {
            margin-top: 20px;
        }

        .footer_icons li {
            display: inline-block;
            margin: 0 10px;

            a > i {
                font-size: 16px;
            }
        }

        .footer_bottom {
            text-align: center;
            margin-top: 40px;
        }
    }
</style>