<!--<template>
  <v-app id="inspire">
    <v-content>
      <v-container fluid fill-height>
        <v-layout align-center justify-center>
          <v-flex xs12 sm8 md4>
            <v-card class="elevation-12">
              <v-toolbar dark color="primary">
                <v-toolbar-title>Login form</v-toolbar-title>
                <v-spacer></v-spacer>
                <v-tooltip bottom>
                  <template v-slot:activator="{ on }">
                    <v-btn :href="source" icon large target="_blank" v-on="on">
                      <v-icon large>code</v-icon>
                    </v-btn>
                  </template>
                  <span>Source</span>
                </v-tooltip>
                <v-tooltip right>
                  <template v-slot:activator="{ on }">
                    <v-btn icon large href="https://codepen.io/johnjleider/pen/wyYVVj" target="_blank" v-on="on">
                      <v-icon large>mdi-codepen</v-icon>
                    </v-btn>
                  </template>
                  <span>Codepen</span>
                </v-tooltip>
              </v-toolbar>
              <v-card-text>
                <v-form>
                  <v-text-field prepend-icon="person" name="login" label="Login" type="text"></v-text-field>
                  <v-text-field id="password" prepend-icon="lock" name="password" label="Password" type="password"></v-text-field>
                </v-form>
              </v-card-text>
              <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn color="primary">Login</v-btn>
              </v-card-actions>
            </v-card>
          </v-flex>
        </v-layout>
      </v-container>
    </v-content>
  </v-app>
</template>-->

<template>
    <v-container class="pt-10 text-center">
      <!--<v-img :src="img/CaptainLogo.jpg"></v-img>-->
      <!--<img src="/img/CaptainLogo.png" class="img-fluid" style="width:35%">-->
      <v-form @submit.prevent="handleSubmit">
        <legend>ป้อนรหัสก่อนเข้าใช้งาน</legend>
        <v-text-field v-model="form.username" label="รหัสเข้าระบบ" name="username" placeholder="กรุณาป้อนชื่อเข้าใช้งาน" />
        <v-text-field
          v-model="form.password"
          label="รหัสผ่าน"
          name="password"
          type="password"
          placeholder="กรุณาป้อนรหัสผ่าน"
        />
        <v-btn type="submit">ยืนยัน</v-btn>
      </v-form>    
    </v-container>
  </template>
  
  <script setup>
  import { reactive } from "vue";
  
  const form = reactive({
    username: "",
    password: "",
  });
  
  const handleSubmit = () => {
    // make api request
    console.log(form);
  };
  </script>