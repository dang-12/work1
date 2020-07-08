<template>
  <div>
    <h1 v-t="'สมุดบันทึกกิจกรรม'" />
    <nuxt-link to="/menu">
      <v-btn block color="light-green accent-2" dark>กลับหน้าหลัก</v-btn>
    </nuxt-link>
    <div class="my-2">
      <nuxt-link to="/ex01">
        <v-btn x-large color="success" dark>กลับหน้าlogin</v-btn>
      </nuxt-link>
    </div>
  </div>
</template>
