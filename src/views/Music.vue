<template>
  <div>
    <transition name="fade" mode="out-in" appear>
      <div v-if="show">
        <TrackItem1
          v-for="track in tracks1"
          v-bind:key="track.id"
          v-bind:title="track.title"
          v-bind:img="track.img"
          v-bind:alt="track.alt"
          v-bind:links="track.links"
        />
        <TrackItem2
          v-for="track in tracks2"
          v-bind:key="track.id"
          v-bind:title="track.title"
          v-bind:img="track.img"
          v-bind:alt="track.alt"
          v-bind:links="track.links"
        />
        <Footer />
      </div>
    </transition>
  </div>
</template>

<script>
// Components
import TrackItem1 from "../components/Track-Item1";
import TrackItem2 from "../components/Track-Item2";
import Footer from "../components/Footer.vue";

// Track Cover Art
import img1 from "../assets/Focus.jpg";
import img2 from "../assets/HM.png";
import img3 from "../assets/Catharsis.jpg";
import img4 from "../assets/VA2.jpg";
import img5 from "../assets/WW.jpg";
import img6 from "../assets/Vanity.jpg";

// Social Media Icons
import icon1 from "../assets/Spotify.svg";
import icon2 from "../assets/BC.svg";
import icon3 from "../assets/SC.svg";
import icon4 from "../assets/YT.svg";

export default {
  name: "Music",
  components: {
    TrackItem1,
    TrackItem2,
    Footer,
  },
  data() {
    return {
      show: true,
      tracks1: [
        {
          id: 0,
          title: "Vanity",
          img: img6,
          alt: "Vanity Cover Art",
          links: [
            {
              id: 0,
              link: "https://jjvy.bandcamp.com/track/vanity",
              platform: "Stream on Bandcamp",
              style: "blue",
              icon: icon2,
            },
            {
              id: 1,
              link: "https://soundcloud.com/jjvy/vanity",
              platform: "Stream on Soundcloud",
              style: "orange",
              icon: icon3,
            },
          ],
        },
        {
          id: 1,
          title: "Focus",
          img: img1,
          alt: "Focus Cover Art",
          links: [
            {
              id: 2,
              link: "https://soundcloud.com/jjvy/focus",
              platform: "Stream on SoundCloud",
              style: "orange",
              icon: icon3,
            },
            {
              id: 3,
              link: "https://www.youtube.com/watch?v=VtKu1CeNYJA",
              platform: "Stream on YouTube",
              style: "red",
              icon: icon4,
            },
          ],
        },

        {
          id: 2,
          title: "Hate Myself",
          img: img2,
          alt: "Hate Myself Cover Art",
          links: [
            {
              id: 4,
              link: "https://soundcloud.com/jjvy/hate-myself",
              platform: "Stream on SoundCloud",
              style: "orange",
              icon: icon3,
            },
            {
              id: 5,
              link: "https://www.youtube.com/watch?v=lgaAOGmEBr8",
              platform: "Stream on YouTube",
              style: "red",
              icon: icon4,
            },
          ],
        },

        {
          id: 3,
          title: "White Walls",
          img: img5,
          alt: "White Walls Cover Art",
          links: [
            {
              id: 6,
              link: "https://soundcloud.com/jjvy/white-walls",
              platform: "Stream on SoundCloud",
              style: "orange",
              icon: icon3,
            },
            {
              id: 7,
              link: "https://www.youtube.com/watch?v=Lccxr9naihw",
              platform: "Stream on YouTube",
              style: "red",
              icon: icon4,
            },
          ],
        },
      ],

      tracks2: [
        {
          id: 3,
          title: "Catharsis",
          img: img3,
          alt: "Catharsis Cover Art",
          links: [
            {
              id: 1,
              link: "https://open.spotify.com/album/2QlSW6N3wDwVH3lijuwSkD?si=vgVvLw1DQTWkot--At-OHA",
              platform: "Stream on Spotify",
              style: "green",
              icon: icon1,
            },
            {
              id: 2,
              link: "https://jjvy.bandcamp.com/track/catharsis",
              platform: "Stream on Bandcamp",
              style: "blue",
              icon: icon2,
            },
            {
              id: 3,
              link: "https://soundcloud.com/jjvy/catharsis",
              platform: "Stream on SoundCloud",
              style: "orange",
              icon: icon3,
            },
            {
              id: 4,
              link: "https://www.youtube.com/watch?v=lgaAOGmEBr8",
              platform: "Stream on YouTube",
              style: "red",
              icon: icon4,
            },
          ],
        },

        {
          id: 4,
          title: "Vengeful Ambitions (V2)",
          img: img4,
          alt: "vengeful Ambitions (V2) Cover Art",
          links: [
            {
              id: 1,
              link: "https://open.spotify.com/album/61JbbfPm7Srov7DaUVbdnX?si=sT9OOwpVRziL7Lwc2j3jVQ",
              platform: "Stream on Spotify",
              style: "green",
              icon: icon1,
            },
            {
              id: 2,
              link: "https://jjvy.bandcamp.com/track/vengeful-ambitions-v2",
              platform: "Stream on Bandcamp",
              style: "blue",
              icon: icon2,
            },
            {
              id: 3,
              link: "https://soundcloud.com/jjvy/vengeful-ambitions-v2",
              platform: "Stream on SoundCloud",
              style: "orange",
              icon: icon3,
            },
            {
              id: 4,
              link: "https://www.youtube.com/watch?v=PIbgMe_1s8A",
              platform: "Stream on YouTube",
              style: "red",
              icon: icon4,
            },
          ],
        },
      ],
    };
  },
};
</script>

<style>
.music-container {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  align-items: center;
  margin-top: 100px;
  margin-bottom: 150px;
}

.info {
  text-align: left;
  position: relative;
  max-width: 500px;
  min-width: 200px;
}

.artwork {
  display: block;
  width: 100%;
  height: auto;
}

.overlay {
  position: absolute;
  display: flex;
  flex-direction: row;
  bottom: 0;
  background: rgba(0, 0, 0, 0.5);
  color: #f1f1f1;
  width: 100%;
  text-align: left;
}

.overlay h2 {
  padding: 10px;
}

.icon {
  width: 50px;
}

.stream-link {
  display: flex;
  flex-direction: row;
  padding: 10px;
  width: 100%;
  margin-bottom: 20px;
  border: 0px;
  cursor: pointer;
}

.green {
  background-color: #1db954;
}

.blue {
  background-color: #54b0c9;
}

.red {
  background-color: #ff0000;
}

.orange {
  background-color: #fe5000;
}

.button-txt {
  font-weight: bolder;
  margin-left: 15px;
  text-transform: uppercase;
}

.fade-enter {
  opacity: 0;
}
.fade-enter-active {
  transition: opacity 1.5s;
}
.fade-leave {
  opacity: 1;
}
.fade-leave-active {
  transition: opacity 1.5s;
  opacity: 0;
}

@media only screen and (max-width: 1050px) {
  .music-container {
    flex-direction: column;
    justify-content: center;
  }

  .buttons {
    margin-top: 50px;
  }

  .info {
    width: 80%;
  }
}
</style>
