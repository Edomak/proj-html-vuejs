<template>
  <div id="app">
    <Header :headerLinks="headerLinks" :icon="icon" />
    <Main />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
import Main from './components/Main.vue';


export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer
  },
  data: function () {
    return {
      headerLinks: [
        "Home",
        "About Me",
        "Testimonials",
        "My Blog",
        "Meetups",
        "Shop",
        "Contact Me"
      ],
      icon: "fas fa-shopping-cart",
    }
  }
}
</script>

<style lang="scss">

@import '~@fortawesome/fontawesome-free/css/all.min.css';

// Common

  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0%;
  }

  .container {
    width: 80%;
    margin: 0 auto;
  }
  .container_60 {
    width: 60%;
    margin: 0 auto;
  }

  body {
    font-family: 'Montserrat', sans-serif;
  }

 // General

  .clearfix::after {
    content: "";
    display: table;
    clear: both;
  }
  .float-left {
    float: left;
  }
  .float-right {
    float: right;
  }

 .green_button {
    background-color: #3da698;
    color: white;
    border-radius: 5px;
    cursor: pointer;
 }
 .orange_button {
    background-color: #f3b329;
    padding: 10px 40px;
    color: white;
    font-size: 10px;
    font-weight: bold;
    text-decoration: none;
    border-radius: 5px;
    cursor: pointer;
}
</style>
