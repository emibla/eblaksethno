<template>
  <v-dialog v-model="dialog">
    <v-card>
      <v-card-title>Besøk hos NASA Houston</v-card-title>
      <v-card-text>
        I 2018 fikk jeg reise med Jenter og teknologi til Houston på besøk til
        NASA. Her fikk jeg treffe astronauter, ingeniører for mange ulike felt,
        flight directors, og mange andre teknologer. Dette var utrolig lærerikt
        og ikke minst motiverende, og i ettertid har jeg holdt flere foredrag om
        besøket. Jeg ble også personlig invitert på en NASA konferanse om Helse
        i verdensrommet av George Abbey, den tidligere direktøren for Johnson
        Space Center.
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
