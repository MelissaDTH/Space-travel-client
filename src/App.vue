<template>
  <v-app>
    <app-navigation v-if="!$route.meta.hideNavigation"></app-navigation>
    <v-content transition="slide-x-transition">
      <router-view></router-view>
      <app-footer v-if="!$route.meta.hideFooter"></app-footer>
    </v-content>
  </v-app>
</template>

<script>
import AppNavigation from '@/components/AppNavigation';
import Footer from '../src/components/Footer';

export default {
  name: 'App',
  components: {
    'app-navigation': AppNavigation,
    'app-footer': Footer
  }
};
</script>
