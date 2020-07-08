<template>
  <div>
    <h1>Hello: {{ name }}</h1>
    <h2>age: {{ age }}</h2>
    <h2>
      name :
      <input type="text" :value="name" />
    </h2>
    <input type="text" :v-model="name" />
    <div>
      <button @click="doSave">SAVE</button>
    </div>
    <div>
      <button @click="doMenu">MAIN MENU</button>
    </div>
    <div>
      <button @click="doHome">HOME</button>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      name: "Alongkorn  phukongka",
      age: 33
    };
  },
  methods: {
    doSave() {
      console.log("DO SAVE");
    },
    doMenu() {
      this.$router.push("/menu");
    },
    doHome() {
      this.$router.push("/");
    }
  }
};
</script>