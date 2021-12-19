<template>
<div class="home">
  <div class="container">
    <div class="home__header">
      <Header />
    </div>
    <Banner />
    <Advantage />
    <Customer />
  </div>
  <div class="footer-wrapper">
    <Footer class="container"></Footer>
  </div>
  
</div>
</template>

<script lang='ts' setup>
import Header from '@/components/header.vue'
import Banner from '@/components/banner.vue'
import Advantage from '@/components/advantage.vue'
import Customer from '@/components/customer.vue'
import Footer from '@/components/Footer.vue'
</script>

<style lang='less' scoped>
.container {
  width: 90%;
  margin: 0 auto;
  max-width: 1094px;
}
.home{
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

</style>