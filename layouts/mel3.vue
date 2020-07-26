<template>
  <!-- App.vue -->

  <v-app>
    <v-navigation-drawer app>
      <!-- -->
    </v-navigation-drawer>

    <v-system-bar dark color="primary">
      <v-spacer></v-spacer>
      <v-icon>mdi-wifi-strength-4</v-icon>
      <v-icon>mdi-signal-cellular-outline</v-icon>
      <v-icon>mdi-battery</v-icon>
      <span>12:30</span>
    </v-system-bar>

    <!-- Sizes your content based upon application components -->
    <v-main>
      <!-- Provides the application the proper gutter -->

      <v-app-bar color="light-blue accent-3" dense dark>
        <nuxt-link to="/mel">
          <v-app-bar-nav-icon></v-app-bar-nav-icon>
        </nuxt-link>

        <v-toolbar-title>Destinations</v-toolbar-title>

        <v-spacer></v-spacer>

        <v-btn icon>
          <v-icon>mdi-magnify</v-icon>
        </v-btn>
      </v-app-bar>
      <!-- If using vue-router -->
      <router-view></router-view>
    </v-main>
  </v-app>
</template>