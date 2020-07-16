<template block color="cyan darken-2">
  <v-card block color="orange lighten-1">
    <v-card-title>
      <h1>Rgister</h1>
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
      <nuxt-link to="/logine">
        <v-btn color="red darken-3" dark>cancel</v-btn>
      </nuxt-link>
      <v-spacer></v-spacer>
      <v-btn color="indigo accent-3" dark>add</v-btn>
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