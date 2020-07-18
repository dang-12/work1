<template>
  <v-container fluid class="pa-0">
    <v-row align="center">
      <v-col cols="12" sm="6">
        <div class="text-center">
          <div class="my-2">
            <nuxt-link to="/line">
              <v-btn color="pink" dark>กิจกรรมเข้าแถว</v-btn>
            </nuxt-link>
          </div>
          <div class="my-2">
            <nuxt-link to="/home">
              <v-btn color="primary" dark>กิจกรรม Homeroom</v-btn>
            </nuxt-link>
          </div>
          <div class="my-2">
            <nuxt-link to="/special">
              <v-btn color="warning" dark>กิจกรรมพิเศษ</v-btn>
            </nuxt-link>
          </div>
          <div>
            <nuxt-link to="/type">
              <v-btn color="error" dark large>กิจกรรมวิชาชีพฯ</v-btn>
            </nuxt-link>
          </div>
          <div class="my-2">
            <nuxt-link to="/#">
              <v-btn color="success" dark>กลับหน้าหลัก</v-btn>
            </nuxt-link>
          </div>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>
