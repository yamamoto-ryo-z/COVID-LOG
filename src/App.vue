<template>
  <div id="app">
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Roboto:wght@100&display=swap"
      rel="stylesheet"
    />
    <headerItem />
    <router-view />
    <hamburger />
    <go-post v-show="this.$route.path !== '/post-page'" />
    <footerItem />
  </div>
</template>

<script>
import hamburger from "../src/components/hamburger.vue"
import headerItem from "../src/components/header.vue"
import footerItem from "../src/components/Footer.vue"
import goPost from "../src/components/Gopost.vue"

export default {
  components: {
    hamburger,
    headerItem,
    footerItem,
    goPost,
  },
}
</script>

<style>
#app {
  font-family: "Roboto", sans-serif;
  overflow-x: hidden;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
