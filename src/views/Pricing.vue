<template>
<div class="pricing">
  <div class="container">
    <div class="pricing__header">
      <Header />
    </div>
    <div class="price-wrapper">
      <div class="info">
        <h1>Pricing</h1>
        <div class="info__text">Start creating beautiful GIFs for free! Upgrade to Pro at anytime to remove the watermark and unlock features.</div>
      </div>
      <price-list></price-list>
      <div class="note">You can cancel at anytime</div>
    </div>
  </div>
  <div class="footer-wrapper">
    <Footer class="container"></Footer>
  </div>
</div>
</template>

<script lang='ts' setup>
import Header from '@/components/header.vue'
import Footer from '@/components/Footer.vue'
import PriceList from '@/components/PriceList.vue'
</script>

<style lang='less' scoped>
.container {
  width: 90%;
  margin: 0 auto;
  max-width: 1094px;
}
.pricing{
  padding-top: 48px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  min-height: 100vh;
  box-sizing: border-box;
  min-width: 900px;
  &__header {
    position: sticky;
    top: 0;
    padding: 24px 0;
    z-index: 10;
    background: #141517;
    opacity: .96;
  }
}
.footer-wrapper {
  background: rgba(0,0,0,0.4);
  height: 100%;
}
.price-wrapper {
  padding: 56px 0 120px;
  .info {
    text-align: center;
    max-width: 580px;
    margin: 0 auto;
    h1 {
      font-size: 60px;
      font-weight: 600;
      margin: 0;
      padding: 0;
      color: #dae1e8;
      line-height: 1.4em;
    }
    &__text {
      margin: 8px 0 0 8px;
      line-height: 1.4em;
      font-size: 22px;
    }
  }
}
.note {
  font-size: 14px;
  line-height: 1.4em;
  font-weight: 400;
  padding-top: 32px;
  text-align: center;
}
</style>