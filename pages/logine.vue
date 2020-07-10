<template block color="cyan darken-2">
  <v-card block color="cyan darken-2">
    <v-card-title>
      <h1>Login</h1>
    </v-card-title>
    <v-card-text>
      <v-form>
        <v-text-field label="Username" prepend-icon="mdi-account-circle" />
        <v-text-field
          :type="showPassword ? 'text' : 'password'"
          label="Password"
          prepend-icon="mdi-lock"
          :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
          @click:append="showPassword = !showPassword"
        />
      </v-form>
    </v-card-text>
    <v-card-actions>
      <nuxt-link to="/Rgister">
        <v-btn color="blue accent-2" dark>Rgister</v-btn>
      </nuxt-link>
      <v-spacer></v-spacer>
      <v-btn color="blue accent-2" dark>Login</v-btn>
    </v-card-actions>
  </v-card>
</template>
<script>
export default {
  name: "App",
  data() {
    return {
      showPassword: false
    };
  }
};
</script>