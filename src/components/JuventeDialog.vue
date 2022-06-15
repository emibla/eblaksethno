<template>
  <v-dialog v-model="dialog">
    <v-card>
      <v-card-title>Lokallagsleder og fylkeskontakt Juvente</v-card-title>
      <v-card-text>
        I ungdomsårene var jeg aktiv i ungdomsorganisasjonen Juvente. Her fikk
        jeg mye ledererfaring, både gjennom ulike lederkurs, som leder for
        lokallaget og gjennom å være leder på flere kurs for ungdom.
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
