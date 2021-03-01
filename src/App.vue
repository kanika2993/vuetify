<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <v-toolbar-title>Vuetify Dashboard</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn text rounded to="/dashboard">Dashboard</v-btn>
      <v-btn text rounded to="/home">Home</v-btn>
      <v-btn text rounded to="/about">About</v-btn>
      <v-btn text rounded to="/login">Login</v-btn>
      <v-btn text rounded to="/login">SignUp</v-btn>      
      <v-btn text rounded to="/login">SignUp</v-btn>

    </v-app-bar>
    <v-content> 
      <router-view ></router-view>   
    </v-content>
    <v-footer dark padless>
      <v-card class="flex" flat tile>
        <v-card-title class="teal">
          <strong class="subheading"
            >Get connected with us on social networks!</strong>

          <v-spacer></v-spacer>

          <v-btn v-for="icon in icons" :key="icon" class="mx-4" dark icon>
            <v-icon size="24px">{{ icon }}</v-icon>
          </v-btn>
        </v-card-title>

        <v-card-text class="py-2 white--text text-center">
          {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
        </v-card-text>
      </v-card>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      icons: ["mdi-facebook", "mdi-twitter", "mdi-linkedin", "mdi-instagram"]
    };
  },
};
</script>