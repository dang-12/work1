<template>
  <center>
    <br>
    <v-card width="750" color="teal orange darken-4">
      <v-card-title-center>

        <h5 >a10</h5>
        <h5 >ทีตั้งจังหวัส : {{ provice }}</h5>
      </v-card-title-center>
      <v-card-text>
        <v-form>
          <v-text-field label="รหัสจังหวัด" v-model="province_id"
                        prepend-icon="mdi-account-circle"
          />
        </v-form>
      </v-card-text>
      <v-card-actions>
        <nuxt-link to="register">
          <v-btn class="ma-2" tile color="amber accent-3" dark>
            REGISTER
          </v-btn>
        </nuxt-link>
        <v-spacer />
        <v-btn class="ma-2" tile color="amber accent-3" dark @click="doSearch">
          LOGIN
        </v-btn>
        </v-btn>
        </v-btn>
      </v-card-actions>
    </v-card>
  </center>
</template>
<script>
export default {
  name: 'App',
  data() {
    return {
      provice:'',
      provice_id: '',
      school: '',
      user: '',
      password: '',
      gpa: '',
    }
  },
  methods: {
    async doSearch() {
      console.log('do search  provice')
      let res = await fetch('http://localhost:7001/provice?province_id=' + this.province_id)
      let data = await res.json()
      console.log(data.rows[0].province_name)
      this.provice=data.rows[0].province_name
    },
  },
}
</script>