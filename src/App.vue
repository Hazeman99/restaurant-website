<template>
  <v-app>
    <Navbar/>
    <router-view></router-view>
    <AppFooter />
  </v-app>
</template>

<script>
import Navbar from './views/Navbar';
import AppFooter from './views/AppFooter';

export default {
  name: 'App',
  components: {
    Navbar,
    AppFooter
  },
  data: () => ({
    //
  }),
};
</script>
