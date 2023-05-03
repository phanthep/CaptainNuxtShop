<template>  
  <v-app>
    <Header/>
      <slot/>
    <Footer/>
  </v-app>
</template>

<script>
  export default {
    data: () => ({ drawer: null }),
  }
</script>