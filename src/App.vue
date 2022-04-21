<template>
  <v-app>
    <v-main>
      <TheNavBar />
      <router-view/>
      <TheFooter />
    </v-main>
  </v-app>
</template>

<script>
import TheNavBar from './components/PageComp/TheNavBar.vue'
import TheFooter from './components/PageComp/TheFooter.vue'
export default {
  name: 'App',
  components: {
    TheNavBar,
    TheFooter
  },
  data: () => ({
    //
  }),
  created() {
    this.$vuetify.theme.dark = true
  }
};
</script>
