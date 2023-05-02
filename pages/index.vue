<template>    
  <v-responsive>
    <v-container fluid tag="section" aria-labelledby="title">            
        <v-row>          
          <v-col cols="12">                        
            <v-carousel
              cycle
              cover
              height="350"
              hide-delimiter-background
              show-arrows="hover"
            >
            <v-carousel-item
              v-for="(item,i) in items"
              :key="i"
              :src="item.src"
              fit
            ></v-carousel-item>
            </v-carousel>
          </v-col>
        </v-row>      
    </v-container>
  </v-responsive>          
</template>

<script>
  definePageMeta({layout: "main-layout"});
// This will work in both `<script setup>` and `<script>`
  export default {    
    data () {
      return {
        items: [          
          {
            src: '/img/carousel/1.png',
          },
          {
            src: '/img/carousel/2.png',
          },
          {
            src: '/img/carousel/3.png',
          },
          {
            src: '/img/carousel/4.png',
          },
          {
            src: '/img/carousel/5.png',
          }
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