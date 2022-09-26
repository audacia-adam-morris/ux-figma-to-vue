<script setup lang="ts">
defineProps<{
  label: string;
  icon: string | null;
}>();
</script>

<template>
  <div class="nav-item">
    <img :src="icon" :alt="label" />
    {{ label }}
  </div>
</template>

<style lang="scss">
.nav-item {
  padding: 8px 28px;
  border-radius: 10px;
  justify-content: center;
  align-items: center;
  display: flex;
  gap: 10px;

  img {
    min-width: 20px;
    display: block;
  }

  &.active,
  &:first-child {
    background: var(--primary-light);
  }
}
</style>
