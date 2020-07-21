<template>
  <!-- App.vue -->

  <v-app>
    <v-system-bar color="teal lighten-2" :height="height" :lights-out="lightsOut" :window="window">
      <v-spacer></v-spacer>
      <v-icon>mdi-wifi-strength-4</v-icon>
      <v-icon>mdi-signal-cellular-outline</v-icon>
      <v-icon>mdi-battery</v-icon>
      <span>12:30</span>
    </v-system-bar>
    <v-navigation-drawer app>
      <!-- -->
    </v-navigation-drawer>

    <div>
      <v-app-bar color="teal darken-4" dense dark>
        <v-toolbar-title>หน้าหลัก</v-toolbar-title>

        <v-btn icon>
          <v-icon>mdi-heart</v-icon>
        </v-btn>
        <v-spacer></v-spacer>
        <v-btn icon>
          <v-icon>mdi-magnify</v-icon>
        </v-btn>

        <v-btn icon>
          <v-icon>mdi-dots-vertical</v-icon>
        </v-btn>
      </v-app-bar>
    </div>

    <!-- Sizes your content based upon application components -->
    <v-main>
      <v-content>
        <nuxt />
      </v-content>
    </v-main>

    <v-footer dark padless>
      <v-card class="flex" flat tile>
        <v-card-title class="teal">
          <v-btn icon="mdi-facebook">
            <v-icon size="24px">{{ icon }}</v-icon>
          </v-btn>
          <v-spacer></v-spacer>
          <v-btn v-for="icon in icons" :key="icon" class="mx-4" dark icon>
            <v-icon size="24px">{{ icon }}</v-icon>
          </v-btn>
        </v-card-title>

        <v-card-text class="py-2 white--text text-center">
          {{ new Date().getFullYear() }} —
          <strong>Vuetify</strong>
        </v-card-text>
      </v-card>
    </v-footer>
  </v-app>
</template>


<script>
export default {
  data: function() {
    return {
      icons: ["mdi-facebook", "mdi-twitter", "mdi-linkedin", "mdi-instagram"]
    };
  }
};
</script>