<template>
  <div style="color: #fff">
    <h1>Show Data Student</h1>
    <v-list-item
      v-for="std in student"
      :key="std.code"
      @click=""
    >
      <v-list-item-avatar>
        <v-img :src="'images/'+std.img" />
      </v-list-item-avatar>
      <v-list-item-content>
        <v-list-item-title v-text="std.code" />
      </v-list-item-content>
      <v-list-item-content>
        <v-list-item-title v-text="std.first_name" />
      </v-list-item-content>
      <v-list-item-content>
        <v-list-item-title v-text="std.last_name" />
      </v-list-item-content>
      <v-list-item-icon>
        <v-icon :color="std.is_active ? 'deep-purple accent-4' : 'grey'">
          chat_bubble
        </v-icon>
      </v-list-item-icon>
    </v-list-item>
    </v-list>
  </div>
</template>
<script>
export default {
  data() {
    return {
      student: [
        {code: '1234567007', frist_name: 'มินตรา', last_name: 'จิตโคตร', is_active: 'Y', avatar: 'images/'},
        {code: '1234567008', frist_name: 'มินตรา', last_name: 'จิตโคตร', is_active: 'Y', avatar: 'https://localhost/static/images/min.jpg'},
      ],
    }
  },
  async created() {
    let res = await this.$http.get('http://localhost:7001/liststd')
    console.log(res.data.row[0].img)
    this.student = res.data.row
  },
}
</script>