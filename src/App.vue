<script setup>
import VFooter from "@/components/VFooter.vue";
import VHeader from "@/components/VHeader.vue";
import VPromo from "@/components/VPromo.vue";
import VClass from "@/components/VClass.vue";
import VHistory from "./components/VHistory.vue";
import VReviews from "./components/VReviews.vue";
import VIdea from "./components/VIdea.vue";
import VPossibilitiesMobile from "./components/VPossibilities-mobile.vue";
import VPossibilities from "./components/VPossibilities.vue";

</script>

<template>
  <v-header />

  <main>
    <v-promo />
    <v-class />
    <v-history/>
    <v-possibilities-mobile/>
    <v-possibilities/>
    <v-idea/>
    <v-reviews/>
  </main>
  <v-footer />
</template>

<style scoped></style>
