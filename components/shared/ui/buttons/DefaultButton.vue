<script lang="ts" setup>
  interface IButtonProps {
    text: string
  };

  const {
    text
  } = defineProps<IButtonProps>();
</script>

<template>
  <div class="button">
    <p>{{ text }}</p>
  </div>
</template>

<style scoped>
  .button {
    height: 44px;
    width: 100%;
    background: #000000;
    color: #FFFFFF;
    font-family: Helvetica;
    font-weight: 400;
    font-size: 11px;
    line-height: 15px;
  }
</style>