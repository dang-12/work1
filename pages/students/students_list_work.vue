<template>
  <v-data-table :headers="headers" :items="desserts" :items-per-page="5" class="elevation-1"></v-data-table>
</template>


<script>
export default {
  data() {
    return {
      headers: [
        {
          text: "code",
          align: "start",
          sortable: false,
          value: "code",
        },
        { text: "created_at", value: "created_at" },
        { text: "update_at", value: "update_at" },

        { text: "id", value: "id" },
      ],
      desserts: [
        {
          code: "01",
          created_at: "โยธิน",
          cupdate_at: "โยธิน",

          id: "โยธิน",
        },
        {
          code: "02",
          created_at: "Yo",
          cupdate_at: "โยธิน",

          id: "โยธิน",
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