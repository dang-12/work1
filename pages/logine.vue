<template>
  <v-card>
    <v-card-title>
      <h1>Login</h1>
    </v-card-title>
    <v-card-text>
      <v-form>
        <v-text-field label="Username" prepend-icon="mdi-account-circle" />
      </v-form>
    </v-card-text>
    <v-card-text>
      <v-form>
        <v-text-field prepend-icon="lock" label="Parssword" append-icon="visibility_off" />
      </v-form>
    </v-card-text>
    <v-card-actions>
      <nuxt-link to="/Rgister">
        <v-btn color="warning" dark>Rgister</v-btn>
      </nuxt-link>
      <v-spacer></v-spacer>
      <v-btn color="error" dark>Login</v-btn>
    </v-card-actions>
  </v-card>
</template>