<template>
  <v-app>
    <skip-links/>
    <profile/>
  
    <v-main id="main">
      <router-view/>
    </v-main>
    <skip-links/>

  </v-app>
</template>

<script>
import skipLinks from './components/skipLinks.vue';
import profile from './components/profile.vue';

export default {
  components: { skipLinks, profile },
  name: 'App',

  data: () => ({
    //
  }),
};
</script>
