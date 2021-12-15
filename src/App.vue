<template>
  <div id="app">
    <AppHeader
      :mainNavLinks="headerMainNavLinks"
      :rigthNavLinks="headerRigthNavLinks"
    />
    <AppMain
      :thumbs="thumbsJumbo"
      :menus="menusInfo"
      :clients="clientsInfo"
    />
    <AppFooter
      :restaurantsInfo="restaurantsInfo"
      :workingTime="workingTime"
    />
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import AppFooter from "./components/AppFooter.vue";

export default {
  name: 'App',
  components: {
    AppHeader,
    AppMain,
    AppFooter
  },
  data() {
    return {
      
      // header

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

      // links rigth nav header
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
      ],

      // main

      // thumbs under jumbo
      thumbsJumbo: [
        'h3-img-1.jpg',
        'h3-img-2.jpg',
        'h3-img-3.jpg',
        'h3-img-4.jpg'
      ],

      // menus info section
      menusInfo: [
        {
          price: '$10',
          name: 'combo piccolo',
          description: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Obcaecati in possimus nobis'
        },
        {
          price: '$20',
          name: 'combo mezzo',
          description: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Obcaecati in possimus nobis'
        },
        {
          price: '$30',
          name: 'combo grande',
          description: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Obcaecati in possimus nobis'
        },
      ],

      // clients section
      clientsInfo: [
        {
          name: 'cowboy',
          logo: 'h1-clients-img-4.png',
          href: '#'
        },
        {
          name: 'gordon street food',
          logo: 'h1-clients-img-3.png',
          href: '#'
        },
        {
          name: 'big cheese',
          logo: 'h1-clients-img-1.png',
          href: '#'
        },
        {
          name: 'bludos bar',
          logo: 'h1-clients-img-2.png',
          href: '#'
        },
        {
          name: 'vegan',
          logo: 'h1-clients-img-5.png',
          href: '#'
        }
      ],

      // footer

      // restautants info
      restaurantsInfo: [
        {
          street: '1614 E. Bell Rd #104.',
          city: 'Salerno, AZ 85022',
          phone: '(602) 867-1010'
        },
        {
          street: '204 E. Pizzetta Tommaso',
          city: 'Sorrento, AZ 85022',
          phone: '(358) 867-1010'
        },
        {
          street: 'Vale Puglia 54',
          city: 'Torre Del Greco, AZ 85022',
          phone: '(359) 867-1010'
        },
        {
          street: 'Corso Itali AA',
          city: 'Naples, AZ 85022',
          phone: '(989) 867-1010'
        },
      ],

      // working time
      workingTime: [
        {
          day: 'monday',
          hours: 'Kitchen Closed'
        },
        {
          day: 'tuesday until friday',
          hours: '9:00 - 22:00'
        },
        {
          day: 'saturday',
          hours: '11am to midnight'
        },
        {
          day: 'sunday',
          hours: '9:00 - 22:00'
        },
      ]
    }
  }
}
</script>

<style lang="scss">
@import '~@fortawesome/fontawesome-free/css/all.min.css';

*{
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}

body {
  font-family: 'Oswald', sans-serif;
  letter-spacing: 1px;
}

a {
  text-decoration: none;
}

ul {
  list-style: none;
}

.btn {
  background-color: #d2401e;
  padding: 10px 30px;
}

section {
  padding: 10px 0;
}

.text_red {
  color: #a43f22;
}

.text_brown {
  color: #ab4027;
}

.text_gray {
  color: #8f8f8f;
}

.text_gold {
  color: #b7903c;
}

.text_orange {
  color: #d2401e;
}

h1, h2, h3, h4, h5, h6 {
  text-transform: uppercase;
}
</style>
