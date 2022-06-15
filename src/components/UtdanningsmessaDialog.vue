<template>
  <v-dialog v-model="dialog">
    <v-card>
      <v-card-title>Foredragsholder for Jenter og teknologi</v-card-title>
      <v-card-text>
        I 2020 ble jeg leid inn av Jenter og teknologi til å stå på stand for
        dem og holde foredrag ved Utdanningsmessa i flere byer rundt om i Norge.
        Dette med formål om å rekruttere flere jenter til å velge
        teknologiutdannelser og tekniske yrkesfag på videregående skole. Her
        programmerte jeg også en microbit robot for å kunne vise frem den og
        koden mens jeg stod på stand.
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
