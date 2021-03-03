<template>
  <v-row justify="center" align="center">
    <v-col cols="12">
      <v-card style="width:100vw">
        <v-img
          height="300"
          src="https://www.sentangsedtee.com/wp-content/uploads/2016/12/2-56-696x462.jpg"
        ></v-img>
        <v-card-title class="headline">
          ปุ๋ยขี้วัว
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
            1. นำมูลสัตว์มาหมักปรับความชื้น 50%
          </p>
          <p style="text-indent: 25px">
            2. นำมูลสัตว์ที่ได้ไปผสมหินฟอสเฟต (K. B. K. 0-3-0) และปุ๋ยยูเรีย (สูตร 46-0-0) เข้าด้วยกัน
          </p>
          <p style="text-indent: 25px">
            3. นำส่วนผสมข้างต้นใส่ลงในถังหมักพร้อมคลุมผ้าปิด รอประมาณ 1 เดือน ก็จะได้ปุ๋ยที่พร้อมแก่การใช้งาน
          </p>
          <p style="text-indent: 25px">
            4. หมั่นพลิกกลับกองปุ๋ยอย่างสม่ำเสมอ โดยจะแบ่งออกเป็น 4 ครั้ง ได้แก่ ครั้งแรกเมื่อหมักได้ 3 วัน ครั้งที่สองเมื่อหมักได้ 10 วัน ครั้งที่สามเมื่อหมักได้ 17 วัน และครั้งที่ 4 เมื่อหมักได้ 24 วันนั่นเอง
          </p>
          <br>
        </v-card-text>
        <v-card-actions>
          <v-btn
            color="error"
            outlined
            nuxt
            to="/freshPlant"
          >
            กลับ(พืชสด)
          </v-btn>
          <v-spacer />
          <v-btn
            color="success"
            nuxt
            to="/grass"
          >
            ไปต่อ(เศษหญ้า)
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
          message: `มูลสัตว์ เช่น ขี้วัว ขี้หมู หรือขี้ไก่ 1,000 กิโลกรัม`,
          color: 'deep-purple lighten-1',
        },
        {
          message: 'หินฟอสเฟต 25 กิโลกรัม',
          color: 'green',
        },
        {
          message: `ปุ๋ยยูเรีย 2 กิโลกรัม`,
          color: 'deep-purple lighten-1',
        }
      ],
  })
}
</script>
