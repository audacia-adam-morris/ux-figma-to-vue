<script setup lang="ts"></script>

<template>
  <div class="cards-container">
    <slot />
  </div>
</template>

<style lang="scss">
$gap: 20px;

.cards-container {
  --card-column-count: 1;

  margin: auto;
  padding: 40px;
  max-width: var(--site-center-width);
  grid-template-columns: repeat(var(--card-column-count), 1fr);
  justify-self: center;
  display: grid;
  gap: $gap;

  @media (min-width: 768px) {
    --card-column-count: 2;
  }

  @media (min-width: 1000px) {
    --card-column-count: 3;
  }
}
</style>
