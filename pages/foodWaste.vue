<template>
  <v-row justify="center" align="center">
    <v-col cols="12">
      <v-card style="width:100vw">
        <v-img
          height="300"
          src="https://www.scb.co.th/content/dam/scb/personal-banking/stories-tips/thai-food/thai-food10.jpg"
        ></v-img>
        <v-card-title class="headline">
          ปุ๋ยจากเศษอาหาร
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
            1. นำถังขนาด 20 ลิตร มาเจาะรูไว้รอบถังแล้วใช้ตาข่ายกันแมลงพันให้รอบ เพื่อช่วยระบายอากาศและป้องกันแมลงรบกวน
          </p>
          <p style="text-indent: 25px">
            2. ผสมเศษอาหารแห้งที่มีขนาดเล็กและไม่มีน้ำ เช่น เศษข้าว เศษขนมปัง ก้างปลา เปลือกไข่ และเปลือกผลไม้ เข้ากับมูลสัตว์ เช่น ขี้วัว ขี้ไก่ ขี้ม้า และเศษใบไม้ ในอัตรา 1:1:1 ส่วน
          </p>
          <p style="text-indent: 25px">
            3. คลุกเคล้าให้เข้ากันแล้วปิดฝาให้สนิท ถ้าหากวันต่อไปมีเศษอาหารเพิ่ม ก็นำมาเติมเข้าไปได้ แต่อย่าลืมผสมในอัตราส่วนเท่าเดิมด้วย
          </p>
          <p style="text-indent: 25px">
            4. พลิกกลับส่วนผสมวันละ 1-2 ครั้ง เป็นประจำทุกวัน
          </p>
          <hr class="my-3">
          <p style="text-indent: 25px">
            <strong>Tips :</strong> ในช่วงแรกไม่จำเป็นต้องเติมน้ำ เพราะเศษอาหารมีความชื้นอยู่แล้ว แต่เมื่อเห็นว่าส่วนผสมเริ่มแห้งลง ก็สามารถพรมน้ำเข้าไปได้เล็กน้อย โดยจะใช้เวลาในการหมักประมาณ 1 เดือน ก็จะได้ปุ๋ยหมักสีดำขนาดเล็ก ที่แห้งสนิทและไม่มีกลิ่นเหม็นไว้ใช้บำรุงต้นไม้แล้ว
          </p>
          <br>
        </v-card-text>
        <v-card-actions>
          <v-btn
            color="error"
            outlined
            nuxt
            to="/"
          >
            กลับ(หน้าหลัก)
          </v-btn>
          <v-spacer />
          <v-btn
            color="success"
            nuxt
            to="/freshPlant"
          >
            ไปต่อ(พืชสด)
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
          message: `เศษอาหารแห้ง เช่น เศษข้าว เศษขนมปัง ก้างปลา เปลือกไข่ เปลือกผลไม้ 1 ส่วน`,
          color: 'deep-purple lighten-1',
        },
        {
          message: 'มูลสัตว์ เช่น ขี้วัว ขี้ไก่ ขี้ม้า 1 ส่วน',
          color: 'green',
        },
        {
          message: `ใบไม้ 1 ส่วน`,
          color: 'deep-purple lighten-1',
        },
        {
          message: 'ถังขนาด 20 ลิตร ',
          color: 'green',
        },
        {
          message: `ตาข่ายกันแมลง`,
          color: 'deep-purple lighten-1',
        },
      ],
  })
}
</script>
