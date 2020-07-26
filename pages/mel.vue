<template >
  <v-app class="white text-center">
    <p></p>
    <p></p>
    <p></p>
    <h1>Welcome!</h1>

    <h2>Lorem ipsum dolor sit amet,</h2>
    <h2>consectetur adipiscing elit.</h2>
    <i class="Fas fa-address-card"></i>
    <p></p>
    <p></p>
    <div>
      <v-card class="grey lighten-1 text-center">
        <v-responsive :aspect-ratio="13/10"></v-responsive>
      </v-card>
    </div>
    <v-card-text>
      <v-container fluid class="pa-0">
        <img src="../images/1.jpg" width="290" height="350" />
      </v-container>
    </v-card-text>
    <p></p>
    <p></p>
    <p></p>
    <p></p>
    <div class="my-2">
      <nuxt-link to="/mel2">
        <v-btn block color="primary" dark>Sign in</v-btn>
      </nuxt-link>
    </div>
  </v-app>
</template>
<script>
export default {
  layout: "mel",
};
</script>
<style scoped>
img {
  position: absolute;
  left: 50px;
  top: 156px;
  z-index: 0;
}
h1 {
  text-align: center;
  color: rgb(0, 0, 0);
  font-size: 25px;
}
h2 {
  color: rgb(71, 70, 70);
  font-size: 13px;
}
</style>