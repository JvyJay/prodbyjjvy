<template>
  <div id="app">
    <Navbar />
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
export default {
  components: {
    Navbar,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@100&display=swap");

#app {
  font-family: "Montserrat", sans-serif;
  text-align: center;
  color: #fff;
  height: 100%;
}

h1 {
  color: #b94242;
  font-weight: bolder !important;
}

h2,
h3,
h4,
h5,
h6 {
  font-size: 1.5rem;
  color: #fff;
}

span,
p {
  font-size: 1rem;
  color: #fff;
}

button {
  text-decoration: none !important;
  font-style: none !important;
  font-weight: bolder !important;
}
.navbar {
  background-color: #000 !important;
}
</style>
