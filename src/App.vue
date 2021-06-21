<template>
  <div id="app">
    <Header />
  </div>
</template>

<script>
import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
    Header
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

  body {
    font-family: 'Montserrat', sans-serif;
  }

 // General

</style>
