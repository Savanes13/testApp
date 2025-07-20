<script lang="ts" setup>
  import { mainIcons } from '../../icons/main';

  interface ISelectProps {
    text: string
  };

  const {
    text
  } = defineProps<ISelectProps>();
</script>

<template>
  <div class="select">
    <div>
      <p>{{ text }}</p>
    </div>
    <div>
      <span
        v-html="mainIcons['plus']"
      ></span>
    </div>
  </div>
</template>

<style scoped>
  .select {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 100%;
    height: 41px;
    border-top: 1px solid #E0E0E0;
    font-weight: 400;
    font-size: 10px;
    line-height: 14px;
    text-transform: uppercase;
    color: #333333;
  }
</style>