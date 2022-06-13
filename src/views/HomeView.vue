<template>
  <v-app-bar>
    <v-btn>Erfaring</v-btn>
    <v-btn @click="$router.r">Prosjekter</v-btn>
  </v-app-bar>
  <about-me-component />
</template>

<script>
import { defineComponent } from "vue";
import AboutMeComponent from "@/components/AboutMeComponent";

export default defineComponent({
  name: "HomeView",

  components: { AboutMeComponent },
});
</script>
