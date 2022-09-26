<script setup lang="ts">
import HeaderComponent from "../components/Base/HeaderComponent.vue";
import CardsContainer from "../components/Base/Cards/CardsContainer.vue";
import CardComponent from "../components/Base/Cards/CardComponent.vue";

const cards = [
  {
    name: "test 1",
  },
  {
    name: "test 2",
  },
  {
    name: "test 3",
  },
  {
    name: "test 4",
  },
];
</script>

<template>
  <HeaderComponent title="Livestock vaccines" />
  <CardsContainer>
    <CardComponent v-for="card in cards" :key="card.name" />
  </CardsContainer>
</template>
