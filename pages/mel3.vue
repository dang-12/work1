<template>
  <v-container>
    <v-row>
      <v-col align="center">
        <v-card color="white">
          <v-card-text color="cyan lighten-4">
            <v-container fluid class="pa-1">
              <v-card class="mx-auto" max-width="350" align="center" color="grey darken-2">
                <v-container fluid class="pa-1">
                  <img src="../images/1.jpg" width="200" height="270" />
                </v-container>
              </v-card>
            </v-container>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
    <v-row>
      <v-col align="center">
        <v-card color="white">
          <v-card-text color="cyan lighten-4">
            <v-container fluid class="pa-1">
              <v-card class="mx-auto" max-width="350" align="center" color="grey darken-2">
                <v-card-title>นายโยธิน นุขุนทด</v-card-title>

                <v-card-subtitle>เกิด 20 กันยายน พศ. 2543</v-card-subtitle>
              </v-card>
            </v-container>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>

    <v-row>
      <v-col align="center">
        <v-card color="white">
          <v-card-text color="cyan lighten-4">
            <v-container fluid class="pa-1">
              <v-card class="mx-auto" max-width="350" align="center" color="grey darken-2">
                <v-card class="mx-auto" max-width="500">
                  <v-card-actions>
                    <v-container>
                      <v-row justify="space-around">
                        <div>
                          <v-btn class="mx-1" color="primary" @click="messages++">
                            <v-icon>thumb_up</v-icon>
                          </v-btn>
                          <v-btn class="mx-1" color="error" @click="messages --">
                            <v-icon>thumb_down</v-icon>
                          </v-btn>
                        </div>
                        <v-spacer></v-spacer>
                        <v-badge :content="messages" :value="messages" color="green" overlap>
                          <v-icon>mdi-heart</v-icon>
                        </v-badge>
                      </v-row>
                    </v-container>

                    <v-btn icon @click="show = !show">
                      <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
                    </v-btn>
                  </v-card-actions>

                  <v-expand-transition>
                    <div v-show="show">
                      <v-divider></v-divider>

                      <v-card-text>บ้านเลขที่ 154 หมู่ 7 ตำบล.กะฮาด อำเถอ.เนินสง่า จังหวัด.ชัยภูมิ รหัสไปรษณีย์ 36130</v-card-text>
                      <v-card-text>กำลังศึกษาอยุ่ : วิทยาลัยเทคนิคชัยภูมิ แผนก เทคโนโลยีสารสนเทศ ระดับชั่น ปวส.2</v-card-text>
                    </div>
                  </v-expand-transition>
                </v-card>
              </v-card>
            </v-container>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>
<script>
export default {
  layout: "mel3",
  data: () => ({
    show: false,
  }),
  data() {
    return {
      messages: 0,
      show: false,
    };
  },
};
</script>
 <style>
#app {
  background: #f5f5f5;
}
img {
  left: 50px;
  top: 156px;
  z-index: 0;
}
</style>