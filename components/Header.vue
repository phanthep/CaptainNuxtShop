<template>
  <!--<v-system-bar>
    <v-spacer></v-spacer>
    <v-icon>mdi-square</v-icon>
    <v-icon>mdi-circle</v-icon>
    <v-icon>mdi-triangle</v-icon>
  </v-system-bar>-->
  <v-app-bar 
    color="teal-darken-4"
    image="img/HomeImage.png">        
    <template v-slot:image>
      <v-img
        gradient="to top right, rgba(19,84,122,.8), rgba(128,208,199,.8)">
      </v-img>
      </template>  
        <template v-slot:prepend>                    
        <v-avatar image="img/CaptainLogo.png" @click.stop="drawer = !drawer"></v-avatar>        
      </template>      
    <v-toolbar-title>ร้านกัปตันพาณิชย์</v-toolbar-title>    
    <v-btn
      v-for="(item,i) in items"          
        :key="i"
        :icon="item.icon"
        variant="text"
        :href="item.link"
        target="_blank">
      </v-btn>
      <!--<a href="https://shop.line.me/@798elirp">
        <v-avatar icon="mdi-vuetify" size="23" image="img/line-green.jpg"></v-avatar>
      </a>-->      
  </v-app-bar>
  <v-navigation-drawer
      v-model="drawer"
      temporary>
      <v-list density="compact" nav>
          <v-list-item @click.stop="ChangeMenu('/')" prepend-icon="mdi-store" title="Home" value="home"></v-list-item>
          <v-list-item @click.stop="ChangeMenu('category')" prepend-icon="mdi-cart-arrow-down" title="Category" value="category"></v-list-item>
          <v-divider></v-divider>
          <v-list-item @click.stop="ChangeMenu('about')" prepend-icon="mdi-pound-box-outline" title="about" value="about"></v-list-item>
      </v-list>
  </v-navigation-drawer>
    <!--<div class="text-center">
    
  </div>
    <v-card max-width="100" class="mx-auto" color="grey-lighten-3">
      <v-app-bar
      </v-app-bar>    
      <v-navigation-drawer v-model="drawer" 
        location="left" permanent>
        <v-list density="compact" nav>
          <v-list-item @click.stop="ChangeMenu('/')" prepend-icon="mdi-home" title="Home" value="home"></v-list-item>
          <v-list-item @click.stop="ChangeMenu('about')" prepend-icon="mdi-account-group-outline" title="about" value="about"></v-list-item>
        </v-list>
      </v-navigation-drawer>          
  </v-card>-->  
</template>

<script>
  export default {
    data: () => ({
      drawer: false,      
      group: null,      
      items: [
        {
          icon: 'mdi-facebook',
          link: 'https://www.facebook.com/Captain.Shop.Bankrut'
        },
        {
          icon: 'mdi-map-marker-circle',
          link: 'https://goo.gl/maps/hFK475ZSPzghMHcq5'
        },
        {
          icon: 'mdi-alpha-l-box-outline',
          //link: 'https://shop.line.me/@798elirp'
          link: 'https://liff.line.me/1645278921-kWRPP32q/?accountId=798elirp'          
        }
      ]      
    }),
    methods: {
            ChangeMenu(page) {
              //alert(page);
              //window.navigator.to(page);
              navigateTo(page, {replace: true})
              //this.drawer  = !this.drawer;
            }
    },
    watch: {
      group () {
        this.drawer = false
      },
    },
  }
</script>