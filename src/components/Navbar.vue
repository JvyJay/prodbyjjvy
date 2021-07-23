<template>
  <div>
    <b-navbar toggleable="lg" type="dark">
      <b-navbar-brand>
        <img src="..\assets\jjvy-logo.png" alt="Logo" width="35" />
        JJVY
      </b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav class="ml-auto">
          <b-nav-item><router-link to="/">Home</router-link></b-nav-item>
          <b-nav-item><router-link to="/music">Music</router-link></b-nav-item>
          <b-nav-item
            ><router-link to="/contact">Contact</router-link></b-nav-item
          >
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
    <router-view />
  </div>
</template>

<script>
export default {
  name: "Navbar",
};
</script>

<style scoped>
a {
  font-weight: bold;
  color: #fff;
  margin: 10px;
  text-decoration: none;
  text-transform: uppercase;
}

a:hover {
  color: #b94242;
  transition: 0.2s ease-in-out;
}
</style>
