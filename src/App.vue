<template>
  <v-app>
    <!-- Conditionally render the app bar based on the current route -->
    <v-app-bar v-if="showAppBar" app color="grey" dark>
      <v-spacer></v-spacer>
      <!-- Logo Section -->
      <v-img
        src="/path/to/your/logo.png"  
        alt="Art Gallery Logo"
        max-height="50"
        class="mr-4"
      ></v-img>
      <v-toolbar-title class="text-wrap">Art Gallery</v-toolbar-title>
      <v-spacer></v-spacer>
    </v-app-bar>

    <v-main>
      <router-view />
    </v-main>

    <v-bottom-navigation app color="darkblue" dark v-if="showbottom">
      <v-btn to="/welcomepage" icon>
        <v-icon>mdi-home</v-icon>
      </v-btn>
      <v-btn to="/gallery" icon>
        <v-icon>mdi-palette</v-icon>
      </v-btn>
      <v-btn to="/exhibitions" icon>
        <v-icon>mdi-calendar</v-icon>
      </v-btn>
      <v-btn to="/contact" icon>
        <v-icon>mdi-account-box</v-icon>
      </v-btn>
    </v-bottom-navigation>
  </v-app>
</template>

<script>
export default {
  name: 'App',
  computed: {
    showAppBar() {
      // List of routes where the app bar should not appear
      const hideRoutes = ['/', '/login', '/register', '/contact'];
      return !hideRoutes.includes(this.$route.path);
    },

     showbottom() {
      // List of routes where the app bar should not appear
      const hideRoutes = ['/', '/login', '/register', ];
      return !hideRoutes.includes(this.$route.path);
    }
  }
};
</script>

<style>
/* Add any global styles here */
</style>
