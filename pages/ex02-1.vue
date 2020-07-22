
<template>
  <div>
    <h1>ชื่อ: {{ first }}</h1>
    <h1>อายุ:{{age}}</h1>
    <h1>รหัสผ่าน:{{password}}</h1>
    <v-col cols="12" sm="6" md="4">
      <v-text-field v-model="first" label="กรุณากรอกชื่อ" filled dense></v-text-field>
    </v-col>

    <v-col cols="12" sm="6">
      <v-text-field
        v-model="age"
        label="อายุ"
        hint="กรุณากรอกอายุของท่าน"
        outlined
        color="red lighten-1"
      ></v-text-field>
    </v-col>
    <v-col cols="12" sm="6">
      <v-text-field
        v-model="password"
        :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
        :rules="[rules.required, rules.min]"
        :type="show1 ? 'text' : 'password'"
        name="input-10-1"
        label="รหัสผ่าน"
        hint="มากกว่า 8  ตัว"
        counter
        @click:append="show1 = !show1"
      ></v-text-field>
    </v-col>
  </div>
</template>
<script>
export default {
  data: function() {
    return {
      name: "alongkorn",
      age: "",
      dep: "information  technology",
      first: "นาย ",
      password: ""
    };
  },
  data() {
    return {
      show1: false,
      show2: true,
      show3: false,
      show4: false,
      rules: {
        required: value => !!value || "รหัสผ่าน",
        min: v => v.length >= 8 || "น้อยกว่า 8 ตัว",
        emailMatch: () => "The email and password you entered don't match"
      }
    };
  }
};
</script>
