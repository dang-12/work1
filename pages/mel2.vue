<template>
  <v-app>
    <p></p>
    <p></p>
    <p></p>
    <p></p>
    <p></p>
    <p></p>
    <p></p>
    <p></p>
    <p></p>
    <v-card-text>
      <v-container fluid class="pa-0">
        <img src="../images/1.jpg" />
      </v-container>
    </v-card-text>

    <p></p>
    <v-col cols="12">
      <v-card block color="indigo lighten-4">
        <v-card-text>
          <v-form>
            <v-text-field label="Username" />
            <v-text-field
              :type="showPassword ? 'text' : 'password'"
              label="Password"
              :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
              @click:append="showPassword = !showPassword"
            />
          </v-form>

          <v-container fluid class="black--text text--lighten-1">
            <v-row class="child-flex">
              <v-col cols="12" sm="6" md="4">
                <v-checkbox v-model="hover" label="Remember me" hide-details></v-checkbox>
              </v-col>
            </v-row>
          </v-container>

          <div class="my-2">
            <nuxt-link to="/mel3">
              <v-btn block color="primary" dark>Sign in</v-btn>
            </nuxt-link>
          </div>
        </v-card-text>
      </v-card>
    </v-col>
  </v-app>
</template>
<script>
export default {
  layout: "mel2",
  name: "App",
  data() {
    return {
      showPassword: false,
    };
  },
};
</script>
<style scoped>
img {
  width: 25%;
  border-radius: 100%;
  position: absolute;
  left: 150px;
  top: 50px;
  z-index: 1;
}
</style>
