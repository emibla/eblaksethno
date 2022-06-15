<template>
  <v-dialog v-model="dialog">
    <v-card>
      <v-card-title>Gjørno' aktivitetsforslag</v-card-title>
      <v-card-text>
        I emnet TDT4140 var vi en gruppe som laget en nettside for
        aktivitetsforslag. Vi brukte rammeverkene react til frontend og strapi
        til backend. Jeg laget designet og jobbet for det meste med frontend. Vi
        brukte parprogrammering underveis i prosjektet, og jobbet stort sett to
        og to sammen.
        <br />Gjennom prosjektet brukte vi Scrum som arbeidsmetode, og jeg fikk
        prøve meg som Scrum master en periode. <br /><br />
        Link til repoet finner du
        <v-btn onclick="window.open('https://github.com/emibla/Gjorno')"
          >her</v-btn
        >
      </v-card-text>
      <v-card-actions>
        <v-btn color="purple" block @click="emitCloseDialog()">Lukk</v-btn>
      </v-card-actions>
    </v-card>
  </v-dialog>
</template>

<script lang="ts" setup>
import { ref, defineEmits } from "vue";
const dialog = ref(false);

//for å sende fra child til parent, dialog til component, må vi emit ("rope")
const emit = defineEmits(["closeDialog"]);

//denne emitter ("roper")
const emitCloseDialog = () => {
  dialog.value = false;
  emit("closeDialog");
};
</script>

<style scoped></style>
