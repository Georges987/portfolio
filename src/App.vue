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
#App {
  background: black;
}

.router-link-active {
  color: red;
}
</style>