<template>
  <v-row justify="center" align="center">
    <v-col cols="12">
      <v-card style="width:100vw">
        <v-img
          height="300"
          src="https://static5-th.orstatic.com/userphoto/Article/0/1A/00094646D30B86CB7AA617j.jpg"
        ></v-img>
        <v-card-title class="headline">
          ปุ๋ยจากปลา
        </v-card-title>
        <v-card-text>
          <h3>วัสดุอุปกรณ์</h3>
          <v-timeline
            align-top
            dense
          >
            <v-timeline-item
              v-for="(mat, i) in materials"
              :key="i"
              :color="mat.color"
              small
            >
              <div>{{ mat.message }}</div>
            </v-timeline-item>
          </v-timeline>
          <hr class="my-3">
          <h3>วิธีทำ</h3>
          <p style="text-indent: 25px">
            1. ละลายหัวเชื้อปุ๋ยหมักซุปเปอร์ พด.2 กับน้ำอุ่น 20 ลิตร
          </p>
          <p style="text-indent: 25px">
            2. นำไปใส่ถังขนาด 200 ลิตร พร้อมทั้งใส่เศษปลา 40 กิโลกรัม และกากน้ำตาล 20 กิโลกรัม ลงไปด้วย
          </p>
          <p style="text-indent: 25px">
            3. ระหว่างหมักให้คนทุกวัน วันละ 2-3 ครั้งต่อวัน อีกทั้งในช่วงที่หมัก น้ำจะลดลงเรื่อย ๆ ให้คอยเติมน้ำสะอาดลงไปอีกด้วย
          </p>
          <p style="text-indent: 25px">
            4. ระยะเวลาในการหมักนานประมาณ 25-30 วัน หรือจนกระทั่งได้ปุ๋ยน้ำหมักจากปลาที่เป็นสีน้ำตาลเข้ม มีฟองละเอียดมาก และมีกลิ่นคล้ายแอลกอฮอล์ จึงค่อยนำมาใช้งาน
          </p>
          <hr class="my-3">
          <p style="text-indent: 25px">
            <strong>Tips :</strong> ถ้าหากฉีดตามใบพืช ให้ผสมปุ๋ยน้ำจากปลา 1 ลิตร เข้ากับน้ำ 100-150 ลิตร แล้วรดประมาณสัปดาห์ละครั้ง แต่ถ้าหากราดลงโคนพืช ให้ผสมปุ๋ยน้ำจากปลา 1 ลิตร เข้ากับน้ำ 50 ลิตร แล้วรดประมาณปีละ 3-4 ครั้ง
          </p>
          <br>
        </v-card-text>
        <v-card-actions>
          <v-btn
            color="error"
            outlined
            nuxt
            to="/grass"
          >
            กลับ(หญ้า)
          </v-btn>
          <v-spacer />
          <v-btn
            color="success"
            nuxt
            to="/"
          >
            กลับหน้าหลัก
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'

export default {
  components: {
    Logo,
    VuetifyLogo
  },
  data: () =>({
    materials: [
        {
          message: `ปลาหรือเศษปลา เช่น หัวปลา ก้างปลา หางปลา พุงปลา 40 กิโลกรัม`,
          color: 'deep-purple lighten-1',
        },
        {
          message: 'กากน้ำตาล 20 กิโลกรัม ',
          color: 'green',
        },
        {
          message: `หัวเชื้อปุ๋ยหมักซุปเปอร์ พด.2 1 ถุง`,
          color: 'deep-purple lighten-1',
        },
        {
          message: 'น้ำสะอาด',
          color: 'green',
        },
        {
          message: `ถังขนาด 200 ลิตร`,
          color: 'deep-purple lighten-1',
        },
      ],
  })
}
</script>
