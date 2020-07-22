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

    <!-- Sizes your content based upon application components -->
    <v-main>
      <!-- Provides the application the proper gutter -->
      <v-container fluid>
        <!-- If using vue-router -->
        <router-view></router-view>
      </v-container>
    </v-main>

    <v-footer dark padless>
      <v-card class="flex" flat tile>
        <v-card-title class="teal">
          <div class="text-center">
            <v-bottom-sheet v-model="sheet" inset>
              <template v-slot:activator="{ on, attrs }">
                <v-btn color="orange" dark v-bind="attrs" v-on="on">กลับหน้าหลัก</v-btn>
              </template>
              <v-sheet class="text-center" height="200px">
                <nuxt-link to="/home1">
                  <v-btn class="mt-6" text color="error" @click="sheet = !sheet">ตกลง</v-btn>
                </nuxt-link>
                <div class="my-3">คุณต้องการกลับหน้าหลัก ใช้ไหม</div>
              </v-sheet>
            </v-bottom-sheet>
          </div>
        </v-card-title>
      </v-card>
    </v-footer>
  </v-app>
</template>
<script>
export default {
  data: () => ({
    sheet: false
  })
};
</script>


