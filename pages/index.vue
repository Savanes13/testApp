<script setup lang="ts">
import MainImage from '~/assets/images/Image.png';
import FirstSmallImage from '~/assets/images/smallimages/Image1.png';
import SecondSmallImage from '~/assets/images/smallimages/Image2.png';
import ThirdSmallImage from '~/assets/images/smallimages/Image3.png';

</script>

<template>
  <div class="product">

    <div class="product__top-block">
      <div class="all-image">
        <div
          class="all-image__item"
          :style="{ backgroundImage: `url(${FirstSmallImage})`}"
        >
        </div>
        <div
           class="all-image__item"
          :style="{ backgroundImage: `url(${SecondSmallImage})`}"
        >
        </div>
        <div
          class="all-image__item"
          :style="{ backgroundImage: `url(${ThirdSmallImage})`}"
        >
        </div>
      </div>
  
      <div 
        class="main-image"
        :style="{ backgroundImage: `url(${MainImage})`}"
      >
      </div>
  
      <div class="info-block">
  
      </div>
    </div>

    <div class="product__bottom-block">

    </div>

  </div>
</template>

<style scoped>
  .product {
    padding: 0px 40px;
  }

  .product__top-block {
    display: flex;
    gap: 30px;
    /* align-items: center; */
  }

  .main-image {
    width: 518px;
    height: 693px;
  }

  .all-image {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 4px;
  }

  .all-image__item {
    width: 70px;
    height: 88px;
  }
</style>