<template>
  <header>
    <div class="container layover_general">
        <div class="header_top">
            <div class="logo">
                <img src="../assets/images/author-logo-round-small.png" alt="Logo Author">
            </div>
            <div class="menu">
                <ul class="right_nav">
                    <li 
                    v-for="(link, index) in headerLinks" :key="index" :class="(link == activeLink)? 'active' : ''" @click.prevent="activePage(index)"><a href="#">{{ link }}</a>
                    </li>
                    <li 
                    :class="(link == activeLink)? 'active' : ''" 
                    @click.prevent="activePage(index)">
                    <a href="#"><i :class="icon"></i></a>
                    </li>
                </ul>
            </div>
        </div>
    </div>
    <div class="hero_text">
        <h1>Damon Vaughr</h1>
        <p>Best selling author and the most influential public intellectual in the western world right now.</p>
        <p id="times">-The New York Times</p>
        <div class="chevron">
            <a href="#"><i class="fas fa-arrow-left"></i></a>
            <a href="#"><i class="fas fa-arrow-right"></i></a> 
        </div>
    </div>
    <div class="book_release">
        <div class="book_img">
            <img src="../assets/images/book-widget.png" alt="book widget">
        </div>
        <div class="book_text">
            <h2>Latest Book Release</h2>
                <h4>D. VAUGHN AUTOBIOGRAPHY</h4>
                <p>Vestibulum tristique turpis in ipsum egestas lobortis. Duis maximus bibendum volutpat. Lorem ipsum dolor sit amet.</p>
        </div>
    </div>
    <div class="book_buttons">
        <a href="#"> <i class="fab fa-amazon"></i> Buy on Amazon</a>
        <a href="#"> <i class="fab fa-apple"></i> Buy on AppStore</a>
    </div>
    <div class="right_button">
        <a href="#"><i class="fas fa-folder"></i>
        <p>Demos</p></a>
        <a href="#"><span class="sales"><span class="dollar">$</span>39</span>
        <p>On Sale</p></a>
    </div>
  </header>
</template>

<script>
export default {
    name: "Header",
    props: {
        headerLinks: Array,
        icon: String
    },
    data: function () {
        return {
            activeLink: "Home",
        }
    },
    methods: {
        activePage: function(index) {
            this.activeLink = this.headerLinks[index];
        }
    }
}
</script>

<style lang="scss" scoped>
    header {
        position: relative;
        height: 500px;
        background-image: url(../assets/images/hero-07-2x.jpg);
        background-size: 84% 108%;
        background-position: -21px -27px;;
    }

    .active {
        border-top: 3px solid #f3b329;
        color: #f3b329;
    }
    a.active {
        color: #f3b329;
    }

    .header_top {
        display: flex;
        justify-content: space-between;
        height: 70px;
        line-height: 70px;

        .logo img {
            position: absolute;
            top: 0;
            right: 85%;
            height: 120px;
        }
    }

    .menu ul {
        display: flex;
        margin-right: 50px;
        list-style: none;

        li {
            margin-left: 30px;
            font-size: 11px;

            a {
                text-decoration: none;
                color: white;

                &.active {
                    color: #f3b329;
                }
                &:hover {
                    color: #f3b329;
                }
            }
        }
    }

    .hero_text {
        position: absolute;
        top: 30%;
        left: 10%;
        width: 450px;
        height: 220px;

        h1 {
            font-family: 'Kristi', cursive;
            margin-bottom: 10px;
            color:#f4b42a;
            font-weight: 100;
            font-size: 35px;
        }

        p {
            color: white;
            font-size: 25px;
            line-height: 38px;
            font-weight: bold;
            font-family: 'DM Serif Display', serif;
        }

        #times {
            color: #868586;
            font-style: italic;
            font-size: 17px;
            margin: 12px 0;
        }

        .chevron i {
            display: inline-block;
            background-color: rgba(0, 0, 0, 0.6); 
            width: 30px;
            height: 30px;
            color: white; 
            text-align: center;
            line-height: 30px;
            font-size: 12px;
            border-radius: 3px;

            &:hover {
                background-color: white;
                color: black;
            }
        }
    }

    .book_release {
        position: absolute;
        display: flex;
        right: 0;
        bottom: 0;
        background-color: white;
        width: 30%;
        padding: 30px 37px;
        font-size: 13px; 

        .book_img img {
            height: 150px;
        }

        .book_text {
             h4 {
                color: #f3b329;
                margin: 10px 0;
                font-size: 12px;
                font-weight: bolder;
            }

            p {
                font-size: 11px;
                line-height: 20px;
                margin: 20px 0;
                color: #34475b;
            }
        }
    }

    .book_buttons {
        position: absolute;
        right: 30px;
        top: 470px;
        z-index: 9999;

        a {
            display: inline-block;
            text-decoration: none; 
            width: 180px;
            padding: 10px 0;
            text-align: center;
            background-color: rgba(120, 207, 196, 0.1);
            border: 1px solid rgba(120, 207, 196, 0.5);
            color: black;
            font-size: 10px;
            border-radius: 5px;

            &:hover {
                border: 2px solid #3da698;
            }
        }

        i {
            margin: 0 5px;
        }
    }

    .right_button {
        position: absolute;
        top: 80px;
        right: 5px;

        a {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            text-decoration: none;
            color: #34475b;
            width: 50px;
            height: 50px;
            background-color: white;
            margin-bottom: 5px;
            border-radius: 5px;
            text-align: center;
            padding: 5px;
            font-size: 10px;
            transition: 0.3s;

            &:hover {
                color: white;
                background-color: #34475b;
            }
        }

        i {
            font-size: 20px;
            transition: 0.3s;

            &:hover {
                color: #3da698;
            }
        }

        .sales {
            font-size: 20px;
            color: #3da698;
            font-weight: bolder;

            &:hover {
                color: #f3b329;
            }
        }

        .dollar {
            position: relative;
            bottom: 8px;
            right: 1px;
            font-size: 13px;
        }
    }

</style>