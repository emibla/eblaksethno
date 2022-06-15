<template>
  <v-dialog v-model="dialog">
    <v-card>
      <v-card-title>Referansegruppe Informasjonsgjenfinning</v-card-title>
      <v-card-text>
        Jeg satt i referansegruppe for TDT4117 Informasjonsgjenfinning høsten
        2021. Jeg syntes dette var ganske interessant spesielt fordi vi måtte
        være med å tilpasse opplegget til å fungere godt digitalt (på grunn av
        coronarestriksjoner) sammen med helt ny foreleser.
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
