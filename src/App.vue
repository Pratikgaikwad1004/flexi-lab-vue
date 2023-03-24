<template>
  <v-app>
      <navbar></navbar>
    <v-main>
      <router-view />
    </v-main>
    <BottomNavbar />
  </v-app>
</template>

<script>
import Navbar from './components/Navbar.vue';
import BottomNavbar from './components/BottomNavbar.vue';
export default {
  name: 'App',

  components: {
    Navbar,
    BottomNavbar
  },

  data: () => ({
    //
  }),
};
</script>

<style>
@import url('@/assets/styles.css');
</style>
