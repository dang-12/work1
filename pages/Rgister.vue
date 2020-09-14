<template block color="cyan darken-2">
  <v-card block color="blue lighten-1">
    <v-card-title>
      <h1>Rgister</h1>
    </v-card-title>
    <v-card-text>
      <v-form>
        <v-text-field label="Username" prepend-icon="mdi-account-circle" />
        <v-text-field
          :type="showPassword ? 'text' : 'password'"
          label="Password"
          prepend-icon="mdi-lock"
          :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
          @click:append="showPassword = !showPassword"
        />
      </v-form>
    </v-card-text>
    <v-card-actions>
      <div class="text-center">
        <v-bottom-sheet v-model="sheet" persistent>
          <template v-slot:activator="{ on, attrs }">
            <v-btn color="green" dark v-bind="attrs" v-on="on">close</v-btn>
          </template>
          <v-sheet class="text-center" height="200px">
            <nuxt-link to="/logine">
              <v-btn class="mt-12" text color="error" @click="sheet = !sheet">ตกลง</v-btn>
            </nuxt-link>
            <div class="py-3">คุณต้องการยกเลิกใช้หรือไม่</div>
          </v-sheet>
        </v-bottom-sheet>
      </div>

      <v-spacer></v-spacer>
      <v-btn color="indigo accent-3" dark>add</v-btn>
    </v-card-actions>
  </v-card>
</template>
<script>
export default {
  layout: "public",
  name: "App",
  data(){
    return {
      showPassword: false
    };
  };
};

export default {
  data: () => ({
    sheet: false
  })
};
</script>
<script>
</script>
