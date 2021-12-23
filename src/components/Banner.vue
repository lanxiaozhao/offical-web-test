<template>
<div class="banner">
  <div class="banner__top">
    <h1>Easily create GIFs</h1>
    <div class="text">Gifmock helps you create high-quality GIFs from static images and mockups.</div>
    <div class="btns">
      <button class="btn btn__download" @click="download()"><img src="/src/assets/icon/heiban.svg" alt="icon" class="icon">Download</button>
      <button class="btn btn__price" @click="goPrice">Buy License…</button>
    </div>
  </div>
  <div class="banner__bottom" >
    <div style="height: 100%;"><swiper
        :modules="modules"
        class="swiper"
        :pagination="{ clickable: true }"
        :autoplay='{
          "delay": 2500,
          "disableOnInteraction": false,
          "pauseOnMouseEnter": true
        }'
        :no-swiping="true"
        :loop="true"
      >
        <swiper-slide class="swiper-item swiper-no-swiping">
          <h1>Create</h1>
          <p>Adjust the delay, size and position of your frames with pixel-perfect precision in just a few clicks.</p>
        </swiper-slide>
        <swiper-slide class="swiper-item swiper-no-swiping">
          <h1>Create</h1>
          <p>Adjust the delay, size and position of your frames with pixel-perfect precision in just a few clicks.</p>
        </swiper-slide>
        <swiper-slide class="swiper-item swiper-no-swiping">
          <h1>Create</h1>
          <p>Adjust the delay, size and position of your frames with pixel-perfect precision in just a few clicks.</p>
        </swiper-slide>
      </swiper></div>
      
    <div class="img"></div>
  </div>
  
</div>
</template>

<script lang='ts' setup>
import { useRouter } from 'vue-router'
import { Pagination, Autoplay } from 'swiper';
import { Swiper, SwiperSlide } from 'swiper/vue'
import 'swiper/css'
import 'swiper/css/pagination';
//SwiperCore.use([Autoplay,Pagination,Navigation]);
  const router = useRouter()
  const goPrice = () => {
    router.push({
      name: 'Pricing'
    })
  }
const download = () => {
    console.log('download')
  }
  const modules= [ Pagination, Autoplay]
</script>

<style lang='less' scoped>
.banner {
  &__bottom {
    display: flex;
    align-items: center;
    padding: 80px 0 150px;
    height: 480px;
    .swiper {
      width: 320px;
      margin-right: 32px;
      height: 100%;
      &-item, :deep(&-slide) {
        display: flex;
        flex-direction: column;
        justify-content: center;
        height: 100%;
        margin-top: -20px;
        h1 {
          margin: 0 0 16px;
          padding: 0;
          font-size: 30px;
          line-height: 1.4em;
          font-weight: 400;
          color: #dae1e8;
        }
        p {
          margin: 0;
          line-height: 1.4em;
          font-weight: 400;
          font-size: 18px;
        }
      }
      :deep(.swiper-pagination-bullet) {
        border: 1px solid #81878d;
        background: transparent;
        box-sizing: border-box;
        &:hover {
          border-color: #fff;
        }
      }
      :deep(.swiper-pagination-bullet-active) {
        background: #00ebcb;
        border: none;
      }
      :deep(.swiper-pagination-bullets) {
        text-align: left;
        bottom: 150px;
      }
    }
    .img {
      flex: 1;
      background: url('../assets/banner.jpg');
      height: 100%;
      background-repeat: no-repeat;
      background-size: cover;
      box-shadow: 0 40px 32px -8px rgba(0,0,0,0.6);
      border-radius: 10px;
    }
  }
  &__top {
    height: calc(100vh - 48px - 76px);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    h1 {
      font-size: 60px;
      font-weight: 600;
      color: #dae1e8;
      margin: 0;
      padding: 0;
    }
    .text {
      margin-top: 8px;
      margin-left: 8px;
      line-height: 1.4em;
      font-weight: 400;
      font-size: 30px;
      width: 580px;
      text-align: center;
    }
    .btns {
      max-width: 580px;
      margin: 32px auto 0;
      display: flex;
      align-items: center;
      justify-content: space-evenly;
      .btn {
        width: 192px;
        height: 48px;
        padding: 0 24px;
        font-size: 18px;
        border-radius: 9px;
        border: none;
        display: flex;
        align-items: center;
        justify-content: center;
        font-weight: 600;
        cursor: pointer;
        &__download {
          margin-right: 8px;
          background: #00ebcb;
          color: #000;
          .icon {
            width: 24px;
            height: 24px;
            margin-right: 6px;
          }
        }
        &__price {
          margin-left: 8px;
          color: #dae1e8;
          background: rgba(234,241,248,0.05);
        }
      }
    }
  }
}

</style>