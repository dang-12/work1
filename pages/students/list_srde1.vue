<template>
  <div>
    <h1>show data student</h1>
    <ul>
      <li v-for="std in student" :key="std.code">
        <span>{{std.code}}</span>
        <span>{{std.first_name}}</span>
        <span>{{std.last_name}}</span>
        <span>{{std.is_active}}</span>
        <v-btn @click="edit(std.code)">EDIT</v-btn>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  data() {
    return {
      student: [
        {
          code: "1234567",
          first_name: "แดง",
          last_name: "dang",
          is_active: "Y",
        },
        {
          code: "1234567",
          first_name: "แดง",
          last_name: "dang",
          is_active: "Y",
        },
      ],
    };
  },
  async created() {
    let res = await this.$http.get("http://localhost:7001/liststd");
    console.log(res.data.row);
    this.student = res.data.row;
  },
  methods: {
    edit(code) {
      console.log(code);
      this.$router.push("edit_formel?code=" + code);
    },
  },
};
</script>
