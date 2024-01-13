<template>
  <main-sk-vue v-if="$route.name == 'home'" :links="links">
    <router-view></router-view>
  </main-sk-vue>
</template>

<script>
import MainSkVue from './components/layout/MainSk.vue'
export default {
  name: 'App',
  components: {
    MainSkVue
  },
  data: () => ({
    links: [
      {
        name: "Home",
        route: '/',
        color: 'text-red',
      },
      {
        name: "About",
        route: '/about',
        color: 'text-purple',
      },
      {
        name: "Services",
        route: '/serve',
        color: 'text-primary',
      },
      {
        name: "Portfolio",
        route: '/portfolio',
        color: 'text-success',
      },
      {
        name: "Blog",
        route: '/blog',
        color: 'text-grey',
      },
      {
        name: "Contact",
        route: '/contact',
        color: 'text-yellow',
      }
    ]
  }),
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.router-link-active {
  color: red;
}

/* Largeur de la barre de défilement */
::-webkit-scrollbar {
  width: 5px;
}

/* Fond de la barre de défilement */
::-webkit-scrollbar-track {
  background-color: black;
}

/* Couleur de la poignée de défilement */
::-webkit-scrollbar-thumb {
  background-color: grey;
  border-radius: 6px;
}

/* Changement de couleur de la poignée de défilement au survol */
::-webkit-scrollbar-thumb:hover {
  background-color: white;
}

</style>