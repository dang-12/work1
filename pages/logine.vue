
<template block color="cyan darken-2">
  <v-card block color="cyan darken-2">
    <v-card-title>
      <h1>Login {{gpa}}</h1>
    </v-card-title>
    <v-card-text>
      <v-form>
        <v-text-field v-model="user" label="Username" prepend-icon="mdi-account-circle" />
        <v-text-field
          :type="showPassword ? 'text' : 'password'"
          label="Password"
          v-model="password"
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
      <v-btn @click="doSave" color="blue accent-2" dark>Login</v-btn>
    </v-card-actions>
  </v-card>
</template>
<script>
export default {
  layout: "default4",
  name: "App",
  data() {
    return {
      showPassword: false,
      user: "",
      password: "",
      gpa: "",
    };
  },
  methods: {
    async doSave() {
      console.log("do save");
      console.log("user:", this.user);
      console.log("password:", this.password);
      //this.$router.push("/Rgister");
      let res = await fetch("http://localhost:7001/list?user=" + this.user);
      let data = await res.json();
      console.log("data=", data.rows[0].GPA);
      this.gpa = data.rows[0].GPA;
    },
  },
};
</script>
