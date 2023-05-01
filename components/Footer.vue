<template>
    <v-footer app
      class="bg-indigo-lighten-1 text-center d-flex flex-column"
    >
      <div>
        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-4"
          :icon="icon"
          variant="text"
        ></v-btn>
      </div>
  
      <div class="pt-0">
        ร้านกัปตันพาณิชย์ รับบัตรธงฟ้าประชารัฐ
      </div>
  
      <v-divider></v-divider>
  
      <div>
        {{ new Date().getFullYear() }} — <strong>ร้านกัปตันพาณิชย์ (ยินดีให้บริการ)</strong>
      </div>
    </v-footer>
  </template>

<script>
export default {
  data: () => ({
    icons: [
      'mdi-facebook',
      'mdi-google'      
    ],
  }),
}
</script>