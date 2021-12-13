<template>
  <div id="app">
    <AppHeader
      :mainNavLinks="headerMainNavLinks"
      :rigthNavLinks="headerRigthNavLinks"
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
      headerMainNavLinks: [
        {
          img: null,
          text: 'home',
          href: '#'
        },
        {
          img: null,
          text: 'pages',
          href: '#'
        },
        {
          img: null,
          text: 'menu',
          href: '#'
        },
        {
          // logo
          img: '/img/logos/h5-logo-divided-header.png',
          text: null,
          href: '#'
        },
        {
          img: null,
          text: 'event',
          href: '#'
        },
        {
          img: null,
          text: 'blog',
          href: '#'
        },
        {
          img: null,
          text: 'landing',
          href: '#'
        },
      ],

      headerRigthNavLinks: [
        {
          img: '/svg/svg-1.svg',
          text: 'cart',
          href: '#'
        },
        {
          img: null,
          text: 'search',
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
