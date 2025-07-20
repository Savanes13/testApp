<script lang="ts" setup>
  interface IColorProps {
    color: string;
    active?: boolean
  };

  const {
    color,
    active = false
  } = defineProps<IColorProps>();
</script>

<template>
  <div class="color">
    <div 
      class="color__block"
      :class="{'color__block--active' : active}"
      :style="{ background: color}"
    ></div>
    <div 
      class="color__activity"
      v-if="active"
    ></div>
  </div>
</template>

<style scoped>
  .color {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 3px;
  }

  .color__block {
    width: 28px;
    height: 27px;
    border: 1px solid transparent;
  }

  .color__block--active {
    border: 1px solid #BDBDBD;
  }

  .color__activity {
    width: 34px;
    height: 1px;
    background: #4F4F4F;
  }
</style>