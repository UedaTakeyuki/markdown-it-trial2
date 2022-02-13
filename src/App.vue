<template>
  <div id="app">
    <Navbar titleStr="Markdown-it" :links="links" />
    <router-view/>
  </div>
</template>

<script>
import {Navbar} from 'vuetify-nav'
export default {
  components: { Navbar},
  data: () => ({
    links: [
      { icon: 'home', text: 'Home', route: '/'},
      { icon: 'face', text: 'About', route: '/about'},
    ]
  }),
};
</script>
