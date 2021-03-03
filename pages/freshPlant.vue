<template>
  <v-row justify="center" align="center">
    <v-col cols="12">
      <v-card style="width:100vw">
        <v-img
          height="300"
          src="https://inwfile.com/s-cb/988nyc.jpg"
        ></v-img>
        <v-card-title class="headline">
          ปุ๋ยจากพืชสด
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
            1. นำพืชสด ซึ่งส่วนใหญ่นิยมเป็นพืชตระกูลทั่ว เช่น ถั่วเขียว ถั่วเหลือง ถั่วลิสง ถั่วนา ถั่วพร้า ปอเทือง โสนคางคก โสนอินเดีย โสนอัฟริกัน หรือพืชตระกูลหญ้าและพืชน้ำ จำนวน 2 กระสอบ มูลสัตว์จำนวน 2 กระสอบ และแกลบดำ 2 กระสอบ มาผสมให้เข้ากัน
          </p>
          <p style="text-indent: 25px">
            2. นำหัวเชื้อจุลินทรีย์ 1 ขัน ผสมเข้ากับน้ำสะอาดประมาณ 40 ลิตร แล้วรดให้ทั่วกองส่วนผสม
          </p>
          <p style="text-indent: 25px">
            3. คลุกให้เข้ากัน หมักไว้ในที่ร่ม รอจนกระทั่งกลายเป็นปุ๋ยที่เย็นแล้วค่อยนำมาใช้งาน
          </p>
          <br>
        </v-card-text>
        <v-card-actions>
          <v-btn
            color="error"
            outlined
            nuxt
            to="/foodWaste"
          >
            กลับ(เศษอาหาร)
          </v-btn>
          <v-spacer />
          <v-btn
            color="success"
            nuxt
            to="/cow"
          >
            ไปต่อ(ขี้วัว)
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
          message: `พืชสด เช่น พืชตระกูลทั่ว พืชตระกูลหญ้า และพืชน้ำ 2 กระสอบ `,
          color: 'deep-purple lighten-1',
        },
        {
          message: 'มูลสัตว์ เช่น ขี้วัว ขี้หมู ขี้เป็ด ขี้ไก่ 2 กระสอบ',
          color: 'green',
        },
        {
          message: `แกลบดำหรือแกลบดิบ 2 กระสอบ`,
          color: 'deep-purple lighten-1',
        },
        {
          message: 'หัวเชื้อจุลินทรีย์ 1 ขัน',
          color: 'green',
        },
        {
          message: `น้ำสะอาด 40 ลิตร`,
          color: 'deep-purple lighten-1',
        },
      ],
  })
}
</script>
