<template >
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

      <v-card>
        <v-toolbar color="primary" dark flat>
          <nuxt-link to="/mel">
            <v-btn icon>
              <v-icon>arrow_back</v-icon>
            </v-btn>
          </nuxt-link>
          <v-toolbar-title>Welcome</v-toolbar-title>

          <v-spacer></v-spacer>

          <v-btn icon>
            <v-icon>mdi-magnify</v-icon>
          </v-btn>

          <v-btn icon>
            <v-icon>mdi-dots-vertical</v-icon>
          </v-btn>

          <template v-slot:extension>
            <v-tabs v-model="model" centered background-color="primary">
              <v-tab v-for="i in 1" :key="i" :href="`#tab-${i}`">SIGN UP</v-tab>
              <v-tab v-for="i in 1" :key="i" :href="`#tab1-${i}`">SIGN IN</v-tab>
            </v-tabs>
          </template>
        </v-toolbar>

        <v-tabs-items v-model="model">
          <v-tab-item v-for="i in 1" :key="i" :value="`tab-${i}`">
            <v-card flat>
              <router-view></router-view>
            </v-card>
          </v-tab-item>

          <v-tab-item v-for="i in 1" :key="i" :value="`tab1-${i}`">
            <v-card flat>
              <router-view></router-view>
            </v-card>
          </v-tab-item>
        </v-tabs-items>
      </v-card>
    </v-main>
  </v-app>
</template>
<script>
export default {
  data() {
    return {
      model: "tab-2",
    };
  },
};
</script>

 <style>
#app {
  background: #f5f5f5;
}
</style>