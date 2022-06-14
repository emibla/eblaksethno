<template>
  <v-dialog v-model="dialog">
    <v-card>
      <v-card-title>Karakterbok</v-card-title>
      <v-card-text>
        I emnet TDT4100 laget jeg en karakterbok. Applikasjonen er bygget etter
        Model, View, Controller prinsippet. I applikasjonen har jeg brukt Java,
        JavaFX for GUI og JUnit5 for testing. Applikasjonen er en karakterbok
        med støtte for flere studenter, hvor hver student kan registrere seg,
        logge inn og registrere ulike emner. Applikasjonen har en tabell med
        oversikt over studentens emner, semesteret og året det ble tatt, samt
        karakter. Studenten kan også se sitt karaktersnitt og sin mediankarakter
        (for ekstra kalkulasjon). Applikasjonen lagrer dataene lokalt i en fil,
        som blir hentet inn ved oppstart av applikasjonen og lagres automatisk
        ved endringer.
        <br /><br />
        Link til repoet finner du
        <v-btn onclick="window.open('https://github.com/emibla/GradeOverview')"
          >her</v-btn
        >
      </v-card-text>
      <v-card-actions>
        <v-btn color="primary" block @click="emitCloseDialog()">Lukk</v-btn>
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
