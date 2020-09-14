<template block color="cyan darken-2">
  <v-card block color="cyan darken-2">
    <v-card-title>
      <h1>สถานศึกษา</h1>
    </v-card-title>
    <v-card-text>
      <v-form>
        <v-text-field v-model="school_id" label="รหัสสถานศึกษา" prepend-icon="mdi-account-circle" />
        <v-text-field v-model="school" label="ชื่อสถานศึกษา " prepend-icon="mdi-account-circle" />
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
      user: "",
      password: "",
      school: "",
      gpa: "",
    };
  },
  methods: {
    async doSave() {
      console.log("do save");
      console.log("user:", this.user);
      console.log("password:", this.password);
      //this.$router.push('/register')
      let res = await fetch(
        "http://localhost:7001/list?school_id=" + this.school_id
      );
      let data = await res.json();
      console.log("data=", data.rows[0].school_name);
      this.school = data.rows[0].school_name;
    },
  },
};
</script>
