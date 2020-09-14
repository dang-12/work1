<template>
  <form>
    <v-text-field v-model="code" label="กาส" />
    <v-text-field v-model="ref_type" label="ชื่อ" />
    <v-text-field v-model="ref_code" label="รหัสกาส" />
    <v-text-field v-model="register_date" label="วันที่" />
    <v-text-field v-model="is_active" label="สถานะ" />
    <v-btn @click="save">บันทึก</v-btn>
    <v-btn>ลบหน้าจอ</v-btn>
  </form>
</template>
<script>
export default {
  data() {
    return {
      code: "",
      ref_type: "",
      ref_code: "",
      register_date: "",
      is_active: "",
    };
  },
  async created() {
    console.log(this.$route.query.code);
    let res = await this.$http.get(
      "http://localhost:7001/editstdel?code=" + this.$route.query.code
    );
    console.log(res.data.res);
    this.code = res.data.row[0].code;
    this.ref_type = res.data.row[0].ref_type;
    this.ref_code = res.data.row[0].ref_code;
    this.register_date = res.data.row[0].register_date;
    this.is_active = res.data.row[0].is_active;
  },
  methods: {
    async save() {
      let card = {
        code: this.code,
        ref_type: this.ref_type,
        ref_code: this.ref_code,
        register_date: this.register_date,
        is_active: this.is_active,
      };
      console.log("card", card);
      let res = await this.$http.post("http://localhost:7001/inserte1", card);
      console.log(res.data.card);
    },
  },
};
</script>
