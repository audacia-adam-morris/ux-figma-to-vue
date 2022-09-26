<script setup lang="ts">
defineProps({
  title: String,
  logo: String | undefined,
});
</script>

<template>
  <div class="header">
    <div class="header__inner">
      <div class="title">
        {{ title }}
      </div>
      <div class="logo">
        <!-- <img :src="logo" :alt="title" /> -->
      </div>
    </div>
  </div>
</template>

<style lang="scss">
.header {
  border-bottom: 1px solid rgba(0, 0, 0, 0.1);
  justify-content: center;
  display: flex;

  &__inner {
    flex-grow: 1;
    width: 100%;
    padding: 40px 40px;
    max-width: var(--site-center-width);
    align-items: center;
    display: flex;

    .title {
      flex-grow: 1;
      font-size: 1.4rem;
      font-weight: 600;
    }

    .logo {
      width: 200px;
      height: 120px;
      background: gray;
    }
  }
}
</style>
