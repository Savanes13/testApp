<script setup lang="ts">
import MainImage from '~/assets/images/Image.png';
import FirstSmallImage from '~/assets/images/smallimages/Image1.png';
import SecondSmallImage from '~/assets/images/smallimages/Image2.png';
import ThirdSmallImage from '~/assets/images/smallimages/Image3.png';
import { mainIcons } from '~/components/shared/icons/main';
import DefaultButton from '~/components/shared/ui/buttons/DefaultButton.vue';
import ProductSize from '~/components/shared/ui/size/ProductSize.vue';
import ProductColor from '~/components/shared/ui/color/ProductColor.vue';
import DefaultSelect from '~/components/shared/ui/select/DefaultSelect.vue';
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
        <div class="info-block__name">
          <p>Жакет удлинённый, белый</p>
        </div>

        <div class="info-block__price">
          <p>8900 RUB</p>
        </div>

        <div class="info-block__size-block">
          <div class="sizes-name">
            <p>Размеры</p>
          </div>
          <div class="sizes-items">
            <ProductSize
              text="xs"
              quantity="мало"
            />
            <ProductSize
              text="s"
            />
            <ProductSize
              text="m"
              :disabled="true"
              quantity="подписка"
            />
          </div>
        </div>

        <div class="info-block__colors-block">
          <div class="colors-name">
            <p>Цвет: белый</p>
          </div>
          <div class="colors-items">
            <ProductColor
              color="#FFFFFF"
              :active="true"
            />
            <ProductColor
              color="#000000"
            />
            <ProductColor
              color="#F9F1DC"
            />
          </div>
        </div>

        <div class="info-block__buttons-block">
          <div class="add-button">
            <DefaultButton
              text="добавить в корзину"
            />
          </div>
          <div class="favorite-button">
            <span
              v-html="mainIcons['stroke']"
            ></span>
          </div>
        </div>

        <div class="info-block__select-block">
          <DefaultSelect
            text="Описание"
          />
          <DefaultSelect
            text="Состав и уход"
          />
        </div>
      </div>


    </div>


    <div class="product__bottom-block">

      <div>
        <div
        
        ></div>
        <div>
          <p>Платье с v-образным вырезом, белый</p>
        </div>
        <div>
          <div>
            <p>14 900 RUB</p>
          </div>
          <div>
            <p>8 000 RUB</p>
          </div>
        </div>
      </div>

      <div>
        <div
        
        ></div>
        <div>
          <p>Жакет двубортный, серо-голубой</p>
        </div>
        <div>
          <div>
            <p>8900 RUB</p>
          </div>
        </div>
      </div>

      <div>
        <div
        
        ></div>
        <div>
          <p>Платье макси с ярусами, белый</p>
        </div>
        <div>
          <div>
            <p>10 500 RUB</p>
          </div>
        </div>
      </div>

      <div>
        <div
        
        ></div>
        <div>
          <p>Комбинезон со стойкой, чёрный</p>
        </div>
        <div>
          <div>
            <p>9500 RUB</p>
          </div>
        </div>
      </div>

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

  .info-block__name {
    font-weight: 400;
    font-size: 12px;
    line-height: 16px;
    text-transform: uppercase;
    margin-bottom: 8px;
  }

  .info-block__price {
    font-weight: 400;
    font-size: 12px;
    line-height: 16px;
    text-transform: uppercase;
    margin-bottom: 31px;
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

  .info-block__size-block {
    margin-bottom: 36px;
  }

  .sizes-name {
    font-weight: 400;
    font-size: 10px;
    line-height: 14px;
    color: #4F4F4F;
    margin-bottom: 8px;
  }

  .sizes-items {
    display: flex;
    align-items: center;
    gap: 14px;
  }

  .info-block__colors-block {
    margin-bottom: 36px;
  }

  .colors-name {
    font-weight: 400;
    font-size: 10px;
    line-height: 14px;
    color: #4F4F4F;
    margin-bottom: 6px;
  }


  .info-block__buttons-block {
    display: flex;
    align-items: center;
    gap: 10px;
    margin-bottom: 40px;
  }

  .add-button {
    width: 306px;
  }

  .favorite-button {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 44px;
    height: 44px;
    border: 1px solid #000000;
    transition: 0.5s ease;
    cursor: pointer;
  }

  .favorite-button:hover {
    background: rgb(241, 241, 241);
  }





  .colors-items {
    display: flex;
    align-items: center;
    gap: 16px;
  }


</style>