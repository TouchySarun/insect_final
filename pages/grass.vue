
<template>
  <v-row justify="center" align="center">
    <v-col cols="12">
      <v-card style="width:100vw">
        <v-img
          height="300"
          src="https://xn--12cmh8bbc4da0bh2bc2a3d5edobk6sg.com/wp-content/uploads/2020/11/12-11-2020-53.jpg"
        ></v-img>
        <v-card-title class="headline">
          ปุ๋ยเศษหญ้า
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
            1. นำเศษหญ้าหรือเศษพืชอื่น ๆ เช่น ฟางข้าว ต้นข้าวโพด หรือต้นอ้อยมาสับให้ละเอียด
          </p>
          <p style="text-indent: 25px">
            2. นำส่วนผสมมากองเป็น 3 ชั้น ในพื้นที่ร่มไร้แสงแดด โดยให้รองพื้นด้วยมูลสัตว์ ตามด้วยเศษหญ้า และปุ๋ยยูเรียทุกชั้น
          </p>
          <p style="text-indent: 25px">
            3. ผสมสารละลาย ประกอบด้วยสารเร่งซุปเปอร์ พด.1 กับน้ำสะอาด 5 ลิตร แล้วนำมาราดบนกองส่วนผสมแต่ละชั้น
          </p>
          <p style="text-indent: 25px">
            4. หาวัสดุมาคลุมพร้อมรดน้ำให้พอชุ่ม คอยดูแลกลับกองปุ๋ยทุก ๆ สัปดาห์ ใช้เวลาในการหมักนานประมาณ 45 วัน ก็จะได้เป็นปุ๋ยหมักชีวภาพที่พร้อมแก่การใช้งาน
          </p>
          <br>
        </v-card-text>
        <v-card-actions>
          <v-btn
            color="error"
            outlined
            nuxt
            to="/cow"
          >
            กลับ(ขี้วัว)
          </v-btn>
          <v-spacer />
          <v-btn
            color="success"
            nuxt
            to="/fish"
          >
            ไปต่อ(ปลา)
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
          message: `เศษหญ้าหรือเศษพืชอื่น ๆ 1,000 กิโลกรัม`,
          color: 'deep-purple lighten-1',
        },
        {
          message: 'มูลสัตว์ 200 กิโลกรัม',
          color: 'green',
        },
        {
          message: `ปุ๋ยยูเรีย 2 กิโลกรัม`,
          color: 'deep-purple lighten-1',
        },
        {
          message: 'สารเร่ง พด.1 1 ซอง',
          color: 'green',
        },
        {
          message: `น้ำสะอาด 5 ลิตร`,
          color: 'deep-purple lighten-1',
        }
      ],
  })
}
</script>
