<template>
  <v-dialog v-model="dialog">
    <v-card>
      <v-card-title>Assisterende daglig leder Telia Shop Solsiden</v-card-title>
      <v-card-text>
        Salg, håndtering av servicesaker og ansvar for oppføløging av våre
        øvrige ansatte. Dette har gitt med god trening i å kommunisere med og
        motivere ulike mennesker, som jeg har hatt mye bruk for i
        gruppeprosjekter og lignende. <br /><br />
        Etter at jeg startet å studere har jeg jobbet som deltid ved samme
        butikk.
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
