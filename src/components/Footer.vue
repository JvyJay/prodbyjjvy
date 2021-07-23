<template>
  <div>
    <footer class="bd-footer">
      <div class="container">
        <!-- Logo & Copyright -->
        <div class="child one">
          <img class="logo" src="../assets/jjvy-logo.png" />
          <p>© jjvy 2021. All Rights Reserved.</p>
        </div>
        <!-- Logo & Copyright -->

        <!-- Nav Links -->
        <div class="child two">
          <h3>Links</h3>
          <router-link to="/">Home</router-link>
          <router-link to="/music">Music</router-link>
          <router-link to="/services">Services</router-link>
          <router-link to="/contact">Contact</router-link>
          <router-view />
        </div>
        <!-- Nav Links -->

        <div class="child three">
          <h3>Social Media</h3>
          <!-- Social Media Links -->
          <div class="grandchild">
            <a
              href="https://open.spotify.com/artist/1aInVwoRxj6Dxe0fDjhLU1?si=YdaOQo4-RceEdIVLjLO5Eg&dl_branch=1"
              ><img class="social" v-bind:src="social[0]" alt="Spotify"
            /></a>
            <a href="https://soundcloud.com/jjvy"
              ><img class="social" v-bind:src="social[1]" alt="Soundcloud"
            /></a>
            <a href="https://jjvy.bandcamp.com/"
              ><img class="social" v-bind:src="social[2]" alt="Bandcamp"
            /></a>
            <a href="https://www.youtube.com/channel/UCETF5AdYZvCoOc7VIQ4ORVg"
              ><img class="social" v-bind:src="social[3]" alt="YouTube"
            /></a>
            <a href="https://www.instagram.com/jjvyy_/"
              ><img class="social" v-bind:src="social[4]" alt="Instagram"
            /></a>
            <a href="https://www.reddit.com/user/PRODIJVY/"
              ><img class="social" v-bind:src="social[5]" alt="Reddit"
            /></a>
          </div>
          <!-- Social Media Links -->

          <!-- Contact Info -->
          <div class="child four">
            <h3>Contact Me</h3>
            <p>prodijvy@gmail.com</p>
          </div>
          <!-- Contact Info -->
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
import Vue from "vue";

// Social Icons
import spotify from "../assets/spotify-social.svg";
import soundcloud from "../assets/soundcloud-social.svg";
import bandcamp from "../assets/bandcamp-social.svg";
import youtube from "../assets/youtube-social.svg";
import instagram from "../assets/instagram-social.svg";
import reddit from "../assets/reddit-social.svg";

export default Vue.component("Footer", {
  data() {
    return {
      social: [spotify, soundcloud, bandcamp, youtube, instagram, reddit],
    };
  },
});
</script>

<style scoped>

.container {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  background-color: #000;
  padding: 50px;
  margin: 0;
  width: 100% !important;
  max-width: 100%;
}

.child {
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.one p {
  width: 60%;
  text-align: left;
  margin-top: 20px;
}

.two a {
  margin-bottom: 10px;
}

.three,
.four {
  align-items: flex-start;
}

.grandchild {
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  margin-bottom: 20px;
}

a {
  text-decoration: none;
  color: #fff;
  text-align: left;
}

.logo {
  width: 50px;
}

.social {
  width: 20px;
  margin-left: 10px;
}

h3 {
  margin-bottom: 20px;
  font-weight: bold;
  text-transform: uppercase;
}

@media only screen and (max-width: 1050px) {
  .container {
    flex-direction: column;
    justify-content: flex-start;
    padding-bottom: 0;
  }

  .child {
    justify-content: flex-start;
    align-items: flex-start;
    margin: 0;
  }

  .one,
  .two,
  .three {
    margin-bottom: 50px;
  }

  .four {
    margin-top: 50px;
  }

  .three,
  .four,
  .grandchild {
    align-items: flex-start;
  }
}
</style>
