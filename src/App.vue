<template>
  <v-app>
    <skip-links/>
    <v-container>
      <names/>
    </v-container>
  
    <v-main id="main">
      <router-view/>
    </v-main>
    <skip-links/>

  </v-app>
</template>

<script>
import skipLinks from './components/skipLinks.vue';
import names from './components/names.vue';

export default {
  components: { skipLinks, names },
  name: 'App',

  data: () => ({
    //
  }),
};
</script>
