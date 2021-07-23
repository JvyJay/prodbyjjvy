<template>
  <div>
    <transition name="fade" mode="out-in" appear>
      <div v-if="show">
        <!-- Hero Area -->
        <b-jumbotron header="JVYY" fluid>
          <p>Music Producer, Web Developer, Martial Artist & Lover of Pizza</p>
        </b-jumbotron>
        <!-- Hero Area -->

        <!-- Services Section -->
        <b-container fluid="md">
          <b-row>
            <b-col v-for="service in services" v-bind:key="service.id">
              <img width="40" :src="service.icon" alt="icon" />
              <h2>{{ service.title }}</h2>
              <p>{{ service.desc }}</p>
              <button>
                <a href="mailto:prodijvy@gmail.com">Learn More</a>
              </button>
            </b-col>
          </b-row>
        </b-container>
        <!-- Services Section -->
        <Footer />
      </div>
    </transition>
  </div>
</template>

<script>
// Components
import Footer from "../components/Footer.vue";

// Service Icons
import icon1 from "../assets/mixing-mastering.svg";
import icon2 from "../assets/web-dev-design.svg";
import icon3 from "../assets/music.svg";

export default {
  name: "Home",
  components: {
    Footer,
  },
  data() {
    return {
      show: true,
      services: [
        {
          id: 1,
          icon: icon1,
          title: "Mixing & Mastering",
          desc: "I will mix and master your tracks whether it be a single, EP or even an album",
        },
        {
          id: 2,
          icon: icon2,
          title: "Web Development",
          desc: "I will design and build your very own professional artist website to host your tracks, merch et cetera.. ",
        },
        {
          id: 3,
          icon: icon3,
          title: "Music Promotion",
          desc: "Submit your music for a chance to be featured on the “Demigod Music” channel",
        },
      ],
    };
  },
};
</script>

<style scoped>
.jumbotron {
  background-image: url("../assets/bg.png") !important;
  background-repeat: no-repeat !important;
  background-attachment: fixed !important;
  background-size: cover;
  background-position: center center;
  height: 55vh;
  display: flex;
  align-items: center;
}

.col {
  margin-bottom: 50px !important;
}

h1 {
  color: #fff !important;
}

h2 {
  font-weight: bold !important;
}

.btn {
  text-transform: uppercase !important;
  border: none !important;
  border-radius: none !important;
}

a {
  background-color: #942e2e !important;
  text-decoration: none !important;
  color: #fff !important;
}

h2 {
  color: #b94242;
}

button {
  padding: 10px;
  border: none;
  border-radius: none;
  background-color: #942e2e;
  color: #fff;
  text-transform: uppercase;
  cursor: pointer;
}
</style>
