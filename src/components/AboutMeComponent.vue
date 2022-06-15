<template>
  <v-container class="mt-10 w-75 bg-pink">
    <v-row class="ma-5"> <h1>Velkommen!</h1></v-row>
    <v-row class="ma-5" sm="12" md="6">
      <v-col>
        Heii! <span class="wave">👋</span> Jeg heter Emily. <br /><br />
        Jeg kommer fra Molde, bor i Trondheim og studerer Datateknologi ved NTNU
        med retning Databaser og søk.<br />Jeg er ferdig med tredje året nå, og
        er ferdig sommeren 2024. <br /><br />
        Ved siden av studiene jobber jeg blant annet for Ada NTNU, et prosjekt
        med fokus på å øke kvinneandelen som fullfører enkelte teknologistudier
        ved NTNU. <br />
        <br />
        På fritiden liker jeg å se fotball, strikking og annet kreativt
        håndarbeid, styrketrening og friluftsliv.<br /><br />
        Jeg har laget en hjemmeside for å bli bedre kjent med frontend og få
        litt erfaring med rammeverket Vue.
      </v-col>
      <v-col><v-img src="../assets/D0FDCD3D.jpg" class="ml-5"></v-img></v-col
    ></v-row>
  </v-container>
</template>

<script setup lang="ts"></script>

<style scoped>
/* Kode for wave funnet på https://codepen.io/jakejarvis/pen/pBZWZw*/
.wave {
  animation-name: wave-animation; /* Refers to the name of your @keyframes element below */
  animation-duration: 2.5s; /* Change to speed up or slow down */
  animation-iteration-count: infinite; /* Never stop waving :) */
  transform-origin: 70% 70%; /* Pivot around the bottom-left palm */
  display: inline-block;
}

@keyframes wave-animation {
  0% {
    transform: rotate(0deg);
  }
  10% {
    transform: rotate(14deg);
  } /* The following five values can be played with to make the waving more or less extreme */
  20% {
    transform: rotate(-8deg);
  }
  30% {
    transform: rotate(14deg);
  }
  40% {
    transform: rotate(-4deg);
  }
  50% {
    transform: rotate(10deg);
  }
  60% {
    transform: rotate(0deg);
  } /* Reset for the last half to pause */
  100% {
    transform: rotate(0deg);
  }
}
</style>
