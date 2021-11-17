<template>
  <v-row>
      <v-cols>
          <v-img src="./assets/dark.PNG"></v-img>
      </v-cols>
      <v-cols>
        <profile/>
      </v-cols>
  </v-row>
</template>

<script>
import profile from './components/profile.vue';

export default {
  components: { profile },

}
</script>

<style>

</style>