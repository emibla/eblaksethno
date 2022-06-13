<template>
  <v-app>
    <v-app-bar color="green">
      <v-btn @click="router.push('/')">Home</v-btn>
      <v-btn @click="router.push('experience')">Erfaring</v-btn>
      <v-btn @click="router.push('projects')">Prosjekter</v-btn> </v-app-bar
    ><v-main> <router-view /> </v-main>
  </v-app>
</template>

<script setup lang="ts">
//importerer metoden useRouter fra bibloteket vue-router
import { useRouter } from "vue-router";

//gir metoden et navn
const router = useRouter();
</script>
