<template>
  <v-dialog v-model="dialog">
    <v-card>
      <v-card-title>Medlem PR-gruppa</v-card-title>
      <v-card-text
        >Cogito NTNU er en frivillig studentorganisasjon som jobber for å fremme
        interesse og læring for kunstig intelligens. Jobbet ett semester med PR.
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
