<template>  
  <v-main class="bg-grey-lighten-2">
  <v-container>
    <v-flex xs12 sm6 offset-sm3>
      <v-card>
        <v-img 
          src="img/carousel/1.png"          
        ></v-img>
        <v-card-title primary-title>
          <div>
            <h3 class="headline mb-0">ร้านกัปตันพาณิชย์</h3>
            <div>
              รับบัตรธงฟ้าประชารัฐ <br/>
              อ.	06:30 - 21:30<br/>
              จ.	06:30 - 21:30<br/>
              อ.	06:30 - 21:30<br/>
              พ.	06:30 - 21:30<br/>
              พฤ.	06:30 - 21:30<br/>
              ศ.	06:30 - 21:30<br/>
              ส.	06:30 - 21:30<br/>
              อา.	06:30 - 21:30<br/>
              0654065599<br/>
              https://g.page/r/Ccl5lLFpIePNEBA<br/>
              รับบัตรเครดิต<br/>
              VisaLINE Pay<br/>
              4 ที่นั่ง, Wi-Fi ฟรี, มีที่จอดรถ, มีปลั๊กไฟ<br/>
              77190 Prachuap Khiri Khan 216/4 ม.ธงชัย อ.บางสะพาน จ.ประจวบคีรีขันธ์<br/>
              ร้านกัปตันพาณิชย์<br/>
            </div>
          </div>
        </v-card-title>

        <v-card-actions>
          <!--<v-btn flat color="orange">Share</v-btn>
          <v-btn flat color="orange">Explore</v-btn>-->
        </v-card-actions>
      </v-card>
    </v-flex>
  </v-container>
  </v-main>
</template>

<script>
// This will work in both `<script setup>` and `<script>`
  definePageMeta({layout: "main-layout"});
  export default {
      data () {
        return {
          card_text: 'รับบัตรธงฟ้าประชารัฐ'  +
                     'อ.	06:30 - 21:30' +
                     'จ.	06:30 - 21:30' +
                     'อ.	06:30 - 21:30' +
                     'พ.	06:30 - 21:30' +
                     'พฤ.	06:30 - 21:30' +
                     'ศ.	06:30 - 21:30' +
                     'ส.	06:30 - 21:30' +
                     'อา.	06:30 - 21:30' +
                     '0654065599' +
                     'https://g.page/r/Ccl5lLFpIePNEBA' +
                     'รับบัตรเครดิต' +
                     'VisaLINE Pay' +
                     '4 ที่นั่ง, Wi-Fi ฟรี, มีที่จอดรถ, มีปลั๊กไฟ' +
                     '77190 Prachuap Khiri Khan 216/4 ม.ธงชัย อ.บางสะพาน จ.ประจวบคีรีขันธ์' +
                     'ร้านกัปตันพาณิชย์' +
                     'แนวทางปฏิบัติของทางร้าน'
        }
      }
    }
</script>