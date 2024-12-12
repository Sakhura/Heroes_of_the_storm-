<template>
  <v-app>
    <v-app-bar app color="blue darken-4" dark>
      <v-toolbar-title>Heroes of the Storm</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn color="orange darken-3" @click="$router.push('/heroes')">Ver Héroes</v-btn>
    </v-app-bar>

<v-main>
  <div class="home-background">
    <v-container class="text-center">
      <h1 class="display-1" white--text>Heroes of the Storm</h1>
      <v-btn color="orange darken-3" @click="$router.push('/heroes')">Ver Héroes</v-btn>
    </v-container>
  </div>
</v-main>

<v-footer app color="blue darken-4">
  <span class="white--text">&copy; 2022 Heroes of the Storm</span>
</v-footer>
  </v-app>
</template>

<script>
// @ is an alias to /src


export default {
  name: 'HomeView',
  components: {
    
  }
}
</script>

<style>
.home-background {
  background: url('https://static.heroesofthestorm.com/heroes/yrel/skins/light-of-hope-800.jpg') no-repeat center center fixed;
  background-size: cover;
  height: 100vh;
  filter: brightness(0.5);
}
</style>