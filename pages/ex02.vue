<template>
  <div>
    <h1>HELLO {{ first }}age:{{std}}</h1>
    <v-text-field
      v-model="first"
      label="กรุณากรอกชื่อ"
      placeholder="กรุณากรอกชือของท่าน"
      outlined
      shaped
    ></v-text-field>
  </div>
</template>
<script>
export default {
  data: function() {
    return {
      name: "alongkorn",
      age: 45,
      dep: "information  technology",
      first: "chaiyaphum"
    };
  }
};
</script>
