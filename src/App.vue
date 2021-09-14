<template>
  <v-app>
    <skip-links/>
  
    <v-main id="main">
      <router-view/>
    </v-main>
    <skip-links/>

  </v-app>
</template>

<script>
import skipLinks from './components/skipLinks.vue';

export default {
  components: { skipLinks },
  name: 'App',

  data: () => ({
    //
  }),
};
</script>
