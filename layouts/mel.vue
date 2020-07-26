<template >
  <!-- App.vue -->

  <v-app>
    <v-navigation-drawer app>
      <!-- -->
    </v-navigation-drawer>

    <!-- Sizes your content based upon application components -->
    <v-main>
      <!-- Provides the application the proper gutter -->
      <v-container fluid>
        <!-- If using vue-router -->
        <router-view></router-view>
      </v-container>
    </v-main>
  </v-app>
</template>
 <style>
#app {
  background: white;
}
</style>