<template>
  <v-app>
    <Navigation />

    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>

    <v-footer app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
import Navigation from '~/components/Navigation.vue'

export default {
  components: {
    Navigation
  },
  data () {
    return {
    }
  }
}
</script>

<style scoped>
  .v-tab {
    text-transform:none !important;
  }
</style>
