<template>
  <v-container class="mt-10 w-75 bg-pink">
    <v-row class="ma-5"><h1>Kontakt meg</h1></v-row>
    <v-row class="ma-5">Du finner meg her: </v-row>
    <v-row class="ma-5">
      <v-img
        src="instagram_icon.png"
        max-width="100"
        class="mr-5"
        onclick="window.open('https://www.instagram.com/eblakseth/')"
      ></v-img>
      <v-img
        src="linkedin_icon.png"
        max-width="100"
        class="mr-5"
        onclick="window.open('https://www.linkedin.com/in/emilyblakseth/')"
      ></v-img>
      <v-img
        src="github2_icon.png"
        max-width="100"
        onclick="window.open('https://github.com/emibla')"
      ></v-img>
    </v-row>
  </v-container>
</template>

<script lang="ts" setup></script>

<style scoped></style>
