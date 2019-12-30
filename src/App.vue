<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
          transition="scale-transition"
          width="40"
        />
        <div> Youshell.com </div>
      </div>

      <v-spacer></v-spacer>

      <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
        <span class="mr-2">Latest Release</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>

    <div class='router-div'>
      <div id="nav"> 
        <router-link to="/">Home </router-link> 
        <router-link to="/data">Data </router-link>
        <router-link to="/meizi">Mei Zi </router-link>
        <router-link to="/about">About </router-link>

      </div>
      <router-view/>
    </div>
  </v-app>
</template>

<script>
export default {
  name: "AppYouShell",
  data: () => ({
    //
  })
};
</script>

<style scoped>
  .router-div{
    margin-top: 56px;
    padding: 10px
  }
</style>
