<template>
  <v-app class="bg-pink-lighten-4">
    <v-app-bar color="pink" max-width="500">
      <v-spacer />
      <v-slide-group multiple show-arrows>
        <v-slide-item :key="1" class="ma-5">
          <v-btn @click="router.push('/')">Hjem</v-btn>
        </v-slide-item>
        <v-slide-item :key="2">
          <v-btn @click="router.push('experience')">Erfaring</v-btn>
        </v-slide-item>
        <v-slide-item :key="3">
          <v-btn @click="router.push('projects')">Prosjekter</v-btn>
        </v-slide-item>
        <v-slide-item :key="4">
          <v-btn @click="router.push('contact')">Kontakt meg</v-btn>
        </v-slide-item>
      </v-slide-group></v-app-bar
    ><v-main> <router-view /> </v-main>
    <v-footer class="bg-pink-lighten-4 text-center"
      ><v-spacer /> Juni 2022 <v-spacer />
    </v-footer>
  </v-app>
</template>

<script setup lang="ts">
//importerer metoden useRouter fra bibloteket vue-router
import { useRouter } from "vue-router";

//gir metoden et navn
const router = useRouter();
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Anton&family=Fascinate&family=Kdam+Thmor+Pro&display=swap");

h1 {
  color: #30051b;
  font-size: 50px;
  font-family: "Anton";
  text-size-adjust: 80%;
}
</style>
