<template>
  <div id="app">
    <AppHeader
      :navLinks="headerNavLinks"
    />
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";

export default {
  name: 'App',
  components: {
    AppHeader
  },
  data() {
    return {
      // links main nav header
      headerNavLinks: [
        {
          text: 'home',
          href: '#'
        },
        {
          text: 'pages',
          href: '#'
        },
        {
          text: 'menu',
          href: '#'
        },
        {
          // logo
          img: 'h5-logo-divided-header.png',
          href: '#'
        },
        {
          text: 'event',
          href: '#'
        },
        {
          text: 'blog',
          href: '#'
        },
        {
          text: 'landing',
          href: '#'
        },
      ]
    }
  }
}
</script>

<style lang="scss">
*{
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}

body {
  font-family: 'Oswald', sans-serif;
}

a {
  text-decoration: none;
}

ul {
  list-style: none;
}
</style>
