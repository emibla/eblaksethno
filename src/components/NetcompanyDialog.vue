<template>
  <v-dialog v-model="dialog">
    <v-card>
      <v-card-title>Deltaker Talent Network med Netcompany</v-card-title>
      <v-card-text>
        Våren 2022 var jeg så heldig å få bli med Netcompany til Danmark på
        Talent Network. Her fikk jeg bli bedre kjent med bedriften og treffe
        mange andre utviklere som har jobbet i Netcompany over flere år. Jeg
        fikk også treffe mange andre studenter fra flere land i Europa, knytte
        kontakter og utveksle erfaringer.<br /><br />
        Vi ble delt inn i team, og startet dagen med teambuildingsaktiviteter.
        Etter dette fikk vi utdelt en case som Netcompany har jobbet med, og
        fikk innblikk i hvordan en hverdag som konsulent hos Netcompany vil
        være. Vi hadde møte med en produkteier hvor vi skulle presentere ideene
        våre, lage en konkret plan for hvordan vi ville ha løst casen, hvilke
        ressurser vi ville trengt og et estimat på hvor mye det ville koste og
        hvor lang tid det ville ta å produsere. <br /><br />

        Dette var en veldig lærerik og inspirerende dag, og har gjort meg veldig
        motivert for fremtiden som utvikler.
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
