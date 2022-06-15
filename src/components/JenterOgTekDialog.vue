<template>
  <v-dialog v-model="dialog">
    <v-card>
      <v-card-title>Jenter og teknologi, NHO </v-card-title>
      <v-card-text>
        Gjennom Jenter og teknologi har jeg holdt flere foredrag under Jenter og
        teknologikonferansene i 2018 og 2019. Jeg har hatt spesielt fokus på å
        gjenkjenne kvaliteter ved seg selv som vil gjøre deg til en god
        teknolog, siden det fremdeles er endel fordommer rundt "hva som skal
        til" for å kunne jobbe med teknologi. <br /><br />For eksempel er
        kvaliteter som nysgjerrighet, kreativitet og gode menneskekjennere
        kvaliteter som en god teknolog kan dra godt nytte av, men som mange ofte
        forbinder med andre yrker. <br /><br />Videre har jeg snakket mye om
        hvorfor det er så viktig at vi utdanner flere kvinnelige teknologer, og
        hatt fokus på fjerne fordommer knyttet til hva man kan jobbe med.
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
const emit = defineEmits(["closeDialog"]);

const emitCloseDialog = () => {
  dialog.value = false;
  emit("closeDialog");
};
</script>

<style scoped></style>
