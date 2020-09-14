<template>
  <div>
    <h1>show data card</h1>
    <ul>
      <li v-for="std in card" :key="std.code">
        <span>{{ std.code }}</span>
        <span>{{ std.ref_typee }}</span>
        <span>{{ std.ref_code }}</span>
        <span>{{ std.register_date }}</span>
        <span>{{ std.is_active }}</span>
        <v-btn @click="edit(std.code)">EDIT</v-btn>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  data() {
    return {
      card: [
        {
          code: "1234567",
          ref_type: "แดง",
          ref_code: "dang",
          register_date: "121221",
          is_active: "Y",
        },
        {
          code: "1234567",
          ref_type: "แดง",
          lref_code: "dang",
          register_date: "2324",
          is_active: "Y",
        },
      ],
    };
  },
  async created() {
    let res = await this.$http.get("http://localhost:7001/liststd");
    console.log(res.data.row);
    this.card = res.data.row;
  },
  methods: {
    edit(code) {
      console.log(code);
      this.$router.push("edit_card?code=" + code);
    },
  },
};
</script>
