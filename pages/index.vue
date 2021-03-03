<template>
  <v-row justify="center" align="center">
    <v-col cols="12">
      <v-card style="width:100vw">
        <v-img
          height="300"
          src="https://www.thaihealth.or.th/data/content/2015/10/29765/cms/thaihealth_c_cegkorsuyz59.jpg"
        ></v-img>
        <v-card-title class="headline">
          รู้ทันโรคพืช มาดูแลพืชปลูกของเราอย่างปลอดภัย
        </v-card-title>
        <v-card-text>
          <p style="text-indent: 50px">
            การที่จะปลูกพืชให้เติบโตอย่างแข็งแรงและปลอดภัย ต้องหมั่นดูแลอย่างสม่ำเสมอ เช่น การรดน้ำ การพรวนดิน การกำจัดวัชพืช และการใส่ปุ๋ย
          </p>
          <p style="text-indent: 50px">
            ในปัจจุบันประเทศไทยมีปัญหาเกี่ยวกับปริมาณขยะที่เพิ่มขึ้นและปัญหาการจัดการขยะที่ยังไม่สามารถจะจัดการได้ หน่วยงานต่าง ๆ ทั้งภาครัฐและภาคเอกชนจึงได้มีการรณรงค์ให้ทุกคนช่วยลด คัดแยก และแนะนำวิธีการนำขยะกลับมาใช้ให้เกิดประโยชน์
          </p>
          <p style="text-indent: 50px">
            ทั้งนี้ จากการเก็บรวบรวมข้อมูลของกรมควบคุมมลพิษ พบว่า ในบรรดาขยะมูลฝอยทั้งหมดนั้น ขยะอินทรีย์หรือขยะย่อยสลายถือเป็นประเภทขยะที่มีอยู่มากที่สุด และมีจำนวนเกินครึ่งของจำนวนขยะทั้งหมด ฉะนั้นถ้าหากเราสามารถลดปริมาณขยะประเภทนี้ลงไปได้ ก็จะช่วยลดปริมาณขยะมูลฝอยรวมตามลงไปด้วยเหมือนกัน และหนึ่งในวิธีกำจัดขยะประเภทนี้ก็คือ การนำไปทำเป็นปุ๋ยหมักสำหรับบำรุงดินและปลูกต้นไม้ เช่น มูลสัตว์ เศษอาหาร เศษผัก-ผลไม้ และเศษขยะต่าง ๆ ผ่านกรรมวิธีที่ทำให้วัสดุอินทรีย์ย่อยสลายด้วยจุลินทรีย์
            โดยการใช้ปุ๋ยหมักจะช่วยให้ดินอุดมสมบูรณ์เหมาะแก่การปลูกพืชพันธุ์ต่าง ๆ มีความปลอดภัยเนื่องจากเป็นขยะที่ปราศจากสารเคมี สามารถลดค่าใช้จ่ายในการซื้อปุ๋ย และช่วยลดปริมาณขยะอินทรีย์ด้วย
          </p>
          <div class="text-xs-right">
            <em><small>&mdash; Sarun Suesuwan</small></em>
          </div>
          <hr class="my-3">
          ดูโค้ดบน
          <a
            href="https://github.com/TouchySarun/insect_final"
            target="_blank"
            rel="noopener noreferrer"
          >
            GitHub
          </a>
          <br>
        </v-card-text>
        <v-card-actions>
          <v-spacer />
          <v-btn
            color="success"
            nuxt
            to="/foodWaste"
          >
            ไปต่อ
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
  }
}
</script>
