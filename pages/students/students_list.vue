<template>
  <v-data-table :headers="headers" :items="desserts" :items-per-page="5" class="elevation-1"></v-data-table>
</template>


<script>
export default {
  data() {
    return {
      headers: [
        {
          text: "std_id",
          align: "start",
          sortable: false,
          value: "code",
        },
        { text: "ชื่อ - สกุล", value: "first_name" },
        { text: "สถานะ", value: "is_active" },
      ],
      desserts: [
        {
          std_id: "01",
          fname: "โยธิน",
          status: "เปิดใช้งาน",
        },
        {
          std_id: "02",
          fname: "Yo",
          status: "ยังไม่เปิดใช้งาน",
        },
      ],
    };
  },
  created() {
    this.listStd();
  },
  methods: {
    async listStd() {
      let res = await fetch("http://localhost:7001/listStd");

      let data = await res.json();
      console.log("datas=", data.rows);
      this.desserts = data.rows[0];
    },
  },
};
</script>