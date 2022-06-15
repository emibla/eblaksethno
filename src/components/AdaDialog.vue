<template>
  <v-dialog v-model="dialog">
    <v-card>
      <v-card-title>Prosjektassistent Ada_ntnu</v-card-title>
      <v-card-text>
        Det kan til tider være tøft å være kvinne i et mannsdominert yrke og
        studie, og samfunnet trenger flere kvinnelige teknologer.
        <br /><br />Ada_ntnu jobber for at flere jenter skal fullføre sine
        teknologistudier. Dette gjør vi gjennom å arrangere ulike arrangement
        for studentene ved våre linjer, for eksempel faglige codehubs som CTF og
        workshops i React, sosiale arrangement for at studentene skal knytte nye
        bekjentskap med hverandre, og bedriftskvelder og turnè i både Oslo og
        Trondheim for å bli la studentene bli bedre kjent med næringslivet og
        motivere studentene til å fullføre studiene. <br /><br />
        Dette for å skape arenaer hvor kvinner kan møte andre kvinner i samme
        situasjon, kjenne på at man ikke er alene og øke motivasjonen for å
        fullføre studiene.<br /><br />
        Foto: Kai T. Dragland
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
