<template>
  <JenterOgTekDialog v-model="showJenterDialog" @closeDialog="closeDialogs()" />
  <ItvDialog v-model="showItvDialog" @closeDialog="closeDialogs()" />
  <AdaDialog v-model="showAdaDialog" @closeDialog="closeDialogs()" />
  <BekkDialog v-model="showBekkDialog" @closeDialog="closeDialogs()" />
  <JuventeDialog v-model="showJuventeDialog" @closeDialog="closeDialogs()" />
  <TeliaKSDialog v-model="showTeliaKSDialog" @closeDialog="closeDialogs()" />
  <TeliaDialog v-model="showTeliaDialog" @closeDialog="closeDialogs()" />
  <NasaDialog v-model="showNasaDialog" @closeDialog="closeDialogs()" />
  <CogitoDialog v-model="showCogitoDialog" @closeDialog="closeDialogs()" />
  <RefgruppeDialog
    v-model="showRefgruppeDialog"
    @closeDialog="closeDialogs()"
  />
  <UtdanningsmessaDialog
    v-model="showUtdanningsmessaDialog"
    @closeDialog="closeDialogs()"
  />
  <NetcompanyDialog
    v-model="showNetcompanyDialog"
    @closeDialog="closeDialogs()"
  />
  <v-container class="mt-10 w-75 bg-pink">
    <v-row class="ma-5"> <h1>Min erfaring</h1></v-row>
    <v-row class="ma-5">
      Jeg har erfaring både fra ulike engasjement, verv, fulltidsjobb og
      sommerjobb. <br />Klikk på bildene for å lese mer.
    </v-row>
    <v-row>
      <v-col
        v-for="experience in experiences"
        :key="experience.title"
        sm="8"
        md="6"
      >
        <v-card class="ma-5">
          <v-card-title class="bg-pink-darken-4" v-text="experience.title">
          </v-card-title>
          <v-card-subtitle
            class="bg-pink-darken-4"
            v-text="experience.date"
          ></v-card-subtitle>
          <v-img
            :src="experience.src"
            v-on:click="experience.onClick = !experience.onClick"
          ></v-img>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup lang="ts">
import { ref } from "vue";
import JenterOgTekDialog from "@/components/JenterOgTekDialog.vue";
import ItvDialog from "@/components/ItvDialog.vue";
import AdaDialog from "@/components/AdaDialog.vue";
import BekkDialog from "@/components/BekkDialog.vue";
import JuventeDialog from "@/components/JuventeDialog.vue";
import NetcompanyDialog from "@/components/NetcompanyDialog.vue";
import TeliaKSDialog from "@/components/TeliaKSDialog.vue";
import TeliaDialog from "@/components/TeliaDialog.vue";
import UtdanningsmessaDialog from "@/components/UtdanningsmessaDialog.vue";
import NasaDialog from "@/components/NasaDialog.vue";
import CogitoDialog from "@/components/CogitoDialog.vue";
import RefgruppeDialog from "@/components/RefgruppeDialog.vue";

const showJenterDialog = ref(false);
const showItvDialog = ref(false);
const showAdaDialog = ref(false);
const showBekkDialog = ref(false);
const showJuventeDialog = ref(false);
const showNetcompanyDialog = ref(false);
const showTeliaKSDialog = ref(false);
const showTeliaDialog = ref(false);
const showUtdanningsmessaDialog = ref(false);
const showNasaDialog = ref(false);
const showCogitoDialog = ref(false);
const showRefgruppeDialog = ref(false);

const closeDialogs = () => {
  showJenterDialog.value = false;
  showItvDialog.value = false;
  showAdaDialog.value = false;
  showBekkDialog.value = false;
  showJuventeDialog.value = false;
  showNetcompanyDialog.value = false;
  showTeliaKSDialog.value = false;
  showTeliaDialog.value = false;
  showUtdanningsmessaDialog.value = false;
  showNasaDialog.value = false;
  showCogitoDialog.value = false;
  showRefgruppeDialog.value = false;
};

const experiences = ref([
  {
    title: "Summer Intern hos Bekk",
    date: "Sommer 2022",
    src: "bekk_icon.png",
    onClick: showBekkDialog,
  },
  {
    title: "Prosjektassistent Ada_ntnu",
    date: "Våren 2019-dd",
    src: "ada.jpg",
    onClick: showAdaDialog,
  },
  {
    title: "Deltaker Talent Network Netcompany",
    date: "Mars 2022",
    src: "netcompany.png",
    onClick: showNetcompanyDialog,
  },
  {
    title: "Referansegruppe Informasjonsgjenfinning",
    date: "Høstsemesteret 2021",
    src: "ntnu_icon.png",
    onClick: showRefgruppeDialog,
  },
  {
    title: "Foredragsholder Utdanningsmessa",
    date: "Januar og Februar 2020",
    src: "utdanningsmessa.jpg",
    onClick: showUtdanningsmessaDialog,
  },
  {
    title: "Foredragsholder Jenter og teknologi",
    date: "2018-2019",
    src: "IMG_1250.jpg",
    onClick: showJenterDialog,
  },
  {
    title: "Cogito NTNU",
    date: "Våren 2019",
    src: "cogito_icon.png",
    onClick: showCogitoDialog,
  },
  {
    title: "Besøk hos NASA, Johnson Space Center",
    date: "Oktober 2018",
    src: "nasa.jpg",
    onClick: showNasaDialog,
  },
  {
    title: "Tillitsvalgt ved Institutt IAL",
    date: "2017-2018",
    src: "ntnu_icon.png",
    onClick: showItvDialog,
  },
  {
    title: "Assisterende daglig leder Telia",
    date: "November 2014 - August 2017",
    src: "telia.jpeg",
    onClick: showTeliaDialog,
  },
  {
    title: "Kundekonsulent Telia",
    date: "August 2011 - November 2014",
    src: "telia.jpeg",
    onClick: showTeliaKSDialog,
  },
  {
    title: "Lokallagsleder og fylkeskontakt Juvente",
    date: "2005 - 2010",
    src: "juvente_icon.jpeg",
    onClick: showJuventeDialog,
  },
]);
</script>
<style scoped></style>
