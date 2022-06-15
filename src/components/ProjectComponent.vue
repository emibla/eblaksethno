<template>
  <gjorno-dialog v-model="showGjornoDialog" @closeDialog="closeDialogs()" />
  <grade-overview-dialog
    v-model="showGradeOverviewDialog"
    @closeDialog="closeDialogs()"
  />
  <v-container class="mt-10 w-75 bg-pink">
    <v-row class="ma-5"> <h1>Noen av mine prosjekter</h1></v-row>
    <v-row class="ma-5">
      Klikk på bildene for å lese litt om prosjektene.
    </v-row>
    <v-row>
      <v-col v-for="project in projects" :key="project.title" sm="8" md="6">
        <v-card class="ma-5">
          <v-card-title
            class="bg-pink-darken-4"
            v-text="project.title"
          ></v-card-title>
          <v-img
            v-on:click="project.onClick = !project.onClick"
            :src="project.src"
          ></v-img>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup lang="ts">
import { ref } from "vue";
import GjornoDialog from "@/components/GjornoDialog.vue";
import GradeOverviewDialog from "@/components/GradeOverviewDialog.vue";

const showGjornoDialog = ref(false);
const showGradeOverviewDialog = ref(false);

const closeDialogs = () => {
  showGradeOverviewDialog.value = false;
  showGjornoDialog.value = false;
};

const projects = ref([
  {
    title: "Karakterbok",
    src: "GradeOverview.png",
    onClick: showGradeOverviewDialog,
  },
  {
    title: "Gjørno' aktivitetsforslag",
    src: "gjorno.png",
    onClick: showGjornoDialog,
  },
]);
</script>
<style scoped></style>
