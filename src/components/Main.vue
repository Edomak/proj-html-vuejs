<template>
  <main>
      <section class="meet">
          <h2>More About Damon Vaughn</h2>
          <p>Damon Vaughn is a professor of psychology at the University of Toronto, a clinical psychologist and the author of the multi-million copy bestseller "The story of my life."</p>
          <button class="green_button">Meet The Author</button>
      </section>
      <section class="logos">
          <div class="container_60">
            <img src="../assets/images/ebay-logotan-2x-200x66.png" alt="">
            <img src="../assets/images/audible-logotan-2x-200x66.png" alt="">
            <img src="../assets/images/bb-logotan-2x-200x66.png" alt="">
            <img src="../assets/images/kindlefire-logotan-2x-200x66.png" alt="">
          </div>
      </section>
      <section class="audio clearfix">
          <div class="container_60">
                <div class="audio_img float-left">
                    <img src="../assets/images/audible-app-2x-400x418.png" alt="">
                </div>
                <div class="audio_text float-left">
                    <h3>New Audiobook</h3>
                    <h4>NO TIME TO READ? NO PROBLEM. LISTEN TO IT</h4>
                    <p>Donec fringilla nunc eu turpis dignissim, at euismod sapien tincidunt. Maecenas eleifend congue cursus.</p>
                    <img src="../assets/images/audible-logo.png" alt="">
                    <img src="../assets/images/bn-logo-tall.png" alt="">
                    <img src="../assets/images/kindle-logo-tall.png" alt="">
                </div>
            </div>
      </section>
      <section class="critics">
          <div class="container">
                <div class="critics_top">
                    <h2 class="font-title">What The Critics Say</h2>
                    <p class="green">testimonials from around the world</p>
                    <button class="orange_button">Read All Testimonials</button>
                </div>
                <div class="main_critics">
                    <div class="critics_left"></div>
                    <div class="critics_right"></div>
                </div> 
          </div>
      </section>
  </main>
</template>

<script>
export default {
    name: "Main"
}
</script>

<style lang="scss">

    // Meet section
    .meet {
        padding: 80px 220px;
        text-align: center;
    }

    .meet h2 {
        font-family: 'Kristi', cursive;
        margin-bottom: 10px;
        color:#f4b42a;
        font-weight: 100;
        font-size: 35px;
    }

    .meet p {
        margin: 20px 0;
        font-size: 18px;
        line-height: 30px;
    }

    .meet button {
        padding: 8px 12px;
        font-size: 12px;
        font-weight: bold;
        cursor: pointer;
    }

    // Logos section

    .logos {
        height: 130px;
        line-height: 130px;
        background-color: #fef7e8;
        text-align: center;

        img {
            width: 150px;
            margin: 0 20px;
            vertical-align: middle;
        }
    }

    // Audio Section

    .audio {
        position: relative;
        height: 400px;
        background-image: url(../assets/images/banner.jpg);
        background-color: black;
        background-size: 110%;
        background-position: -100px -50px;

        .audio_img img {
            position: relative;
            top: 65px;
            width: 80%;
        }

        .audio_text {
            position: absolute;
            top: 30%;
            right: 30%;
            width: 400px;
            text-align: center;
            padding: 20px 20px;

            img {
                height: 30px;
                margin: 0 15px;
            }

            h3 {
                color: white;
                font-family: 'DM Serif Display';
                font-size: 25px;
                margin: 20px 0;
            }

            h4 {
                color:#f4b42a;
                font-size: 12px;
                margin: 20px 0;
            }

            p {
                font-size: 12px;
                color: gray;
                margin: 20px 0;
                line-height: 20px;
            }
        }
    }

        // Critics section

        .critics {
            height: 400px;
            padding: 40px 0;

            h2 {
                font-size: 25px;
                margin-bottom: 10px;
            }

            p {
                font-size: 12px;
                text-transform: uppercase;
                color: #3da698;
            }
        }

        .critics_top {
            position: relative;

            button {
                position: absolute;
                right: 0;
            }
        }
</style>