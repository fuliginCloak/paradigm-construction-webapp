<template>
  <v-app>
    <!-- Start of Navigation -->
    <nav>
      <!-- Start of app toolbar -->
      <v-toolbar app>
        <v-toolbar-side-icon
          @click.stop="drawer = !drawer"
          class="hidden-md-and-up"
        ></v-toolbar-side-icon>

        <v-toolbar-title class="hidden-sm-and-down" @click="$router.push('/')"
          >Paradigm Workshop
        </v-toolbar-title>

        <v-spacer></v-spacer>
        <v-toolbar-items class="hidden-sm-and-down">
          <v-btn flat to="/about">About</v-btn>
          <v-btn flat to="/services">Services</v-btn>
          <v-btn flat to="/gallery">Gallery</v-btn>
          <v-btn flat to="/contact">Contact</v-btn>
        </v-toolbar-items>
      </v-toolbar>
      <!-- End of app toolbar -->
    </nav>
    <!-- End of Navigation -->

    <!-- Mobile nav begin -->
    <Slide
      class="hidden-sm-and-up bm-burger-bars"
      :closeOnNavigation="true"
      width="200"
      noOverlay
    >
      <h3>Paradigm</h3>
      <v-space></v-space>

      <v-btn flat small text to="/about">About</v-btn>
      <v-space></v-space>
      <v-btn flat small text to="/services">Services</v-btn>
      <v-space></v-space>
      <v-btn flat small text to="/gallery">Gallery</v-btn>
      <v-space></v-space>
      <v-btn flat small text to="/contact">Contact</v-btn>
    </Slide>

    <v-content>
      <!-- Display view pages here based on route -->
      <router-view></router-view>
    </v-content>
    <!-- FOOTER -->
    <v-bottom-navigation v-model="bottomNav">
      <v-btn icon href="https://www.facebook.com/" target="_blank">
        <v-icon>mdi-facebook</v-icon>
      </v-btn>

      <v-btn icon href="https://twitter.com/?lang=en" target="_blank">
        <v-icon>mdi-twitter</v-icon>
      </v-btn>

      <v-btn icon href="https://www.linkedin.com/" target="_blank">
        <v-icon>mdi-linkedin</v-icon>
      </v-btn>

      <v-btn icon href="https://www.instagram.com/" target="_blank">
        <v-icon>mdi-instagram</v-icon>
      </v-btn>
    </v-bottom-navigation>
  </v-app>
</template>

<script>
import { Slide } from 'vue-burger-menu'

export default {
  components: {
    Slide // Hambuger transition
  }
}
</script>

<style scoped>
.bm-burger-bars {
  background-color: white;
}
</style>
