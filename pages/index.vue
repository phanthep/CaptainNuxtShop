<template>         
  <v-main class="bg-grey-lighten-2">
    <v-container fluid tag="section" aria-labelledby="title">            
        <v-row>          
          <v-col cols="12">                        
            <v-carousel
              cycle
              cover
              height="350"
              interval="3000"
              hide-delimiter-background
              show-arrows="hover"
            >
            <v-carousel-item            
              v-for="(item,i) in carousels"
              :key="i"
              :src="item"
              fit
            ></v-carousel-item>
            </v-carousel>
          </v-col>
        </v-row>      
    </v-container>  
  </v-main>   
</template>

<script>
  definePageMeta({layout: "main-layout"});
// This will work in both `<script setup>` and `<script>`
  export default {    
    data () {
      return {
        carousels: [
          '/img/carousel/1.png',
          '/img/carousel/2.png',
          '/img/carousel/3.png',
          '/img/carousel/4.png',
          '/img/carousel/5.png',
          '/img/carousel/6.png',
          '/img/carousel/7.png',
          '/img/carousel/8.png',
          '/img/carousel/9.png',
        ]
      }
    }    
  }
</script>

<style>
  .v-navigation-drawer {
    z-index: 999999 !important;
  }
</style>