<script lang="ts" setup>
  interface IProductSize {
    text: string,
    quantity?: string | null,
    disabled?: boolean
  };

  const {
    text,
    quantity = null,
    disabled = false
  } = defineProps<IProductSize>();
</script>

<template>
  <div class="size">
    <div 
      class="size-block"
      :class="{'size-block--disabled' : disabled}"
    >
      <p>{{ text }}</p>
    </div>
    <div 
      class="size-quantity"
      :class="{'size-quantity--disabled' : disabled}"
      v-if="quantity"
    >
      <p>{{ quantity }}</p>
    </div>
  </div>
</template>

<style scoped>
  .size {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  .size-block {
    width: 65px;
    height: 31px;
    display: flex;
    align-items: center;
    justify-content: center;
    border: 1px solid #333333;
    color: #333333;
    font-weight: 400;
    font-size: 10px;
    line-height: 14px;
    text-transform: uppercase;
  }

  .size-block--disabled {
    border: 1px solid #BDBDBD;
    color: #BDBDBD;
  }

  .size-quantity--disabled {
    color: #BDBDBD;
  }

  .size-quantity {
    font-weight: 400;
    font-size: 10px;
    line-height: 14px;
    color: #828282;
  } 
</style>