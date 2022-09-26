<script setup lang="ts">
import LogoComponent from "../Base/Nav/LogoComponent.vue";
import AccountComponent from "../Base/Nav/AccountComponent.vue";
import NavItemComponent from "../Base/Nav/NavItemComponent.vue";
import HomeSvg from "../../assets/icons/home.svg";

const navItems = [
  {
    label: "Home",
    icon: HomeSvg,
  },
  {
    label: "Projects",
    icon: HomeSvg,
  },
  {
    label: "Messages",
    icon: HomeSvg,
  },
  {
    label: "Forums",
    icon: HomeSvg,
  },
  {
    label: "Settings",
    icon: HomeSvg,
  },
];
</script>

<template>
  <div class="nav">
    <!-- Logo -->
    <LogoComponent />
    <!-- Nav Items -->
    <div class="nav-items">
      <NavItemComponent
        v-for="item in navItems"
        :key="item.label"
        :label="item.label"
        :icon="item.icon"
      />
    </div>
    <!-- Account -->
    <AccountComponent />
  </div>
</template>

<style lang="scss">
.nav {
  padding: 12px;
  align-items: center;
  justify-content: space-between;
  border-bottom: 1px solid rgba(0, 0, 0, 0.1);
  display: flex;

  .nav-items {
    display: flex;
    gap: 10px;
  }
}
</style>
