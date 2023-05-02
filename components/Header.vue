<template>
    <!--<div class="text-center">
    <NuxtLink class="nav-link active" to="/">Home</NuxtLink>|
    <NuxtLink class="nav-link active" to="category">Category</NuxtLink>|
    <NuxtLink class="nav-link active" to="about">About</NuxtLink> 
  </div>-->    
    <v-card max-width="100" class="mx-auto" color="grey-lighten-3">
      <v-app-bar
        color="teal-darken-4"
        image="img/HomeImage.png"
      >
        <template v-slot:image>
          <v-img
            gradient="to top right, rgba(19,84,122,.8), rgba(128,208,199,.8)"
          ></v-img>
        </template>        
        <template v-slot:prepend>
          <v-avatar image="img/CaptainLogo.png" @click.stop="drawer = !drawer"></v-avatar>
          <!--<v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>-->
        </template>

        <v-app-bar-title>กัปตันพาณิชย์</v-app-bar-title>
        <v-spacer></v-spacer>

        <!--<v-btn icon>
          <v-icon>mdi-magnify</v-icon>
        </v-btn>

        <v-btn icon>
          <v-icon>mdi-heart</v-icon>
        </v-btn>-->
        
        <v-btn
          v-for="(item,i) in items"          
          :key="i"
          :icon="item.icon"
          variant="text"
          :href="item.link"
          target="_blank"          
        ></v-btn>

      </v-app-bar>    
      <v-navigation-drawer v-model="drawer" 
        location="left" permanent>
        <v-list density="compact" nav>
          <v-list-item @click.stop="ChangeMenu('/')" prepend-icon="mdi-home" title="Home" value="home"></v-list-item>
          <!--<v-list-item @click.stop="ChangeMenu('category')" prepend-icon="mdi-account" title="Category" value="category"></v-list-item>-->
          <v-list-item @click.stop="ChangeMenu('about')" prepend-icon="mdi-account-group-outline" title="about" value="about"></v-list-item>
          <!--<v-list-item @click.stop="ChangeMenu('login')" prepend-icon="mdi-account-group-outline" title="login" value="login"></v-list-item>-->
          <!--<NuxtLink class="nav-link active" to="about"><v-list-item @click.stop="ChangeMenu('about')" prepend-icon="mdi-account-group-outline" title="about" value="about"></v-list-item></NuxtLink>-->
        </v-list>
        <!--<img src="img/CaptainLogo.jpg" class="img-fluid" style="size:20%;"><NuxtLink class="nav-link active" to="/">Home</NuxtLink><br/>
        <NuxtLink class="nav-link active" to="category">Category</NuxtLink><br/>
        <NuxtLink class="nav-link active" to="about">About</NuxtLink>-->
        <!--<v-list
          :items="items"
        ></v-list>-->
      </v-navigation-drawer>          
  </v-card>  
</template>

<script>
  export default {
    data: () => ({
      drawer: false,      
      group: null,      
      items: [
        {
          icon: 'mdi-facebook',
          link: 'https://www.facebook.com/Captain.Shop.Bankrut'},
        {
          icon: 'mdi-google',
          link: 'https://goo.gl/maps/hFK475ZSPzghMHcq5'
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