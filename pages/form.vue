<template>
  <v-form ref="form">
    <v-text-field v-model="std_id" :counter="10" label="student_id"></v-text-field>

    <v-text-field v-model="name" :counter="10" label="Name"></v-text-field>

    <v-text-field v-model="lastname" label="Lastname"></v-text-field>

    <v-text-field v-model="GPA" label="GPA"></v-text-field>

    <v-btn :disabled="!valid" color="success" class="mr-4" @click="validate">Validate</v-btn>

    <v-btn color="warning" @click="resetValidation">Reset Validation</v-btn>
  </v-form>
</template>

<script>
export default {
  data: () => ({
    user: "4921010026",
    std_id: "",
    name: "",
    lastname: "",
    GPA: "",
    name: "",
  }),

  methods: {
    async init_load() {
      console.log("welcome");
      let res = await fetch("http://localhost:7001/list?=" + this.user);
      let data = await res.json();
      console.log("data=", data.rows[0].GPA);
      this.GPA = data.rows[0].GPA;
      this.name = data.rows[0].name;
      this.lastname = data.rows[0].lastname;
      this.std_id = data.rows[0].student_id;
    },
  },
  created() {
    this.init_load();
  },
};
</script>
