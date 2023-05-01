<template>
    <div class="text-center">
    <NuxtLink class="nav-link active" to="/">Home</NuxtLink>|
    <NuxtLink class="nav-link active" to="category">Category</NuxtLink>|
    <NuxtLink class="nav-link active" to="about">About</NuxtLink> 
  </div>
    <v-card max-width="448" class="mx-auto" color="grey-lighten-3">    
      <v-app-bar
        color="teal-darken-4"
        image="https://picsum.photos/1920/1080?random"
      >
        <template v-slot:image>
          <v-img
            gradient="to top right, rgba(19,84,122,.8), rgba(128,208,199,.8)"
          ></v-img>
        </template>        
        <template v-slot:prepend>
          <!--<v-img width="50" class="img-circle border-radius: 10%" src="img/CaptainLogo.jpg" @click.stop="drawer = !drawer"></v-img>-->
          <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
        </template>

        <v-app-bar-title>ร้านกัปตันพาณิชย์</v-app-bar-title>

        <v-spacer></v-spacer>

        <v-btn icon>
          <v-icon>mdi-magnify</v-icon>
        </v-btn>

        <v-btn icon>
          <v-icon>mdi-heart</v-icon>
        </v-btn>        
        <NuxtLink class="nav-link active" to="login"><v-btn icon>
          <v-icon>mdi-dots-vertical</v-icon>
        </v-btn></NuxtLink>
      </v-app-bar>    
      <v-navigation-drawer v-model="drawer" 
        location="left" permanent>
        <v-list density="compact" nav>
          <v-list-item prepend-avatar="img/CaptainLogo.png" @click.stop="ChangeMenu('home')" title="Home" value="home"></v-list-item>
          <v-list-item @click.stop="ChangeMenu('account')" prepend-icon="mdi-account" title="My Account" value="account"></v-list-item>
          <v-list-item @click.stop="ChangeMenu('about')" prepend-icon="mdi-account-group-outline" title="about" value="about"></v-list-item>
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
          title: 'Foo',
          prependIcon: 'mdi-home-city',
          value: 'foo',
        },
        {
          title: 'Bar',
          prependIcon: 'mdi-home-city',
          value: 'bar',
        },
        {
          title: 'Fizz',
          prependIcon: 'mdi-home-city',
          value: 'fizz',
        },
        {
          title: 'Buzz',
          value: 'buzz',
        },
      ],
      
    }),
    methods: {
            ChangeMenu(page) {
              //alert(page);
              //window.navigator.to(page);
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