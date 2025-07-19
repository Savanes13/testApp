<script lang="ts" setup>
import { logoIcons } from '~/components/shared/icons/logo';
import { mainIcons } from '~/components/shared/icons/main';
</script>

<template>
  <div class="nav">
    <div class="nav__logo">
      <span
        v-html="logoIcons['mainLogo']"
      >
      </span>
    </div>
    <div class="nav__items">
      <div class="active-item">
        <span
          v-html="mainIcons['search']"
        ></span>
      </div>
      <div class="active-item">
        <span
          v-html="mainIcons['favorite']"
        ></span>
      </div>
      <div class="active-item">
        <span
          v-html="mainIcons['user']"
        ></span>
      </div>
      <div class="active-item">
        <span
          v-html="mainIcons['basket']"
        ></span>
      </div>
    </div>
  </div>
</template>

<style scoped>
  .nav {
    height: 86px;
    display: flex;
    align-items: center;
    justify-content: flex-end;
    position: relative;
    padding: 0px 48px;
  }

  .nav__logo {
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
  }

  .nav__items {
    display: flex;
    align-items: center;
    gap: 16px;
  }
</style>