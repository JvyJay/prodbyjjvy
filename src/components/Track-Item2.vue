/* eslint-disable prettier/prettier */
<template>
  <div v-if="show" class="music-container">
    <div class="info">
      <img class="artwork" :src="img" :alt="alt" />
      <div class="overlay">
        <h2>jjvy - {{ title }}</h2>
      </div>
    </div>
    <div class="buttons">
      <a v-for="link in links" v-bind:key="link.id" :href="link.link">
        <button v-bind:class="link.style" class="stream-link">
          <img class="icon" :src="link.icon" />
          <p class="button-txt">{{ link.platform }}</p>
        </button>
      </a>
    </div>
  </div>
</template>

<script>
import Vue from "vue";

export default Vue.component("TrackItem2", {
  data() {
    return { show: true };
  },
  props: {
    title: String,
    img: String,
    alt: String,
    links: Array,
  },
});
</script>

<style scoped>
p {
  margin-top: 1rem !important;
}
</style>
