<template>
  <v-dialog v-model="dialog">
    <v-card>
      <v-card-title>Tillitsvalgt ved Institutt IAL</v-card-title>
      <v-card-text>
        Mens jeg gikk forkurs ble jeg valgt som tillitsvalgt for Instituttet for
        allmennfag. Min oppgave ble i hovedsak å bidra i planleggingen av
        relokaliseringen og flytting av forkurs opp til Gløshaugen. Jeg var også
        medlem av studentrådet ved IE- fakultetet, hvor vi jobbet med
        problemstillinger tilknyttet virksomheten.
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
