<template>
<div class="footer">
  <div class="footer-item" >
    <h2>产品名称</h2>
    <div class="footer-item__text" @click="goHome">Home</div>
    <div class="footer-item__text" @click="goPrice">Princing</div>
    <div class="footer-item__text" @click="goTerms">Terms</div>
    <div class="footer-item__text" @click="goPrivacy">Privacy</div>
  </div>
</div>
</template>

<script lang='ts' setup>
import { useRouter } from 'vue-router'
  const router = useRouter()
  const goHome = () => {
    router.push({
      name: 'Home'
    })
  }
  const goPrice = () => {
    router.push({
      name: 'Pricing'
    })
  }
  const goTerms = () => {
    router.push({
      name: 'Terms'
    })
  }
  const goPrivacy = () => {
    router.push({
      name: 'Privacy'
    })
  }
</script>

<style lang='less' scoped>
.footer {
  height: 100%;
}
.footer-item {
  padding-bottom: 48px;
  h2 {
    font-weight: 600;
    color: #dae1e8;
    font-size: 14px;
    line-height: 1.4em;
    margin: 0;
    padding: 56px 0 16px;
  }
  &__text {
    padding: 4px 0;
    cursor: pointer;
    &:hover {
      color: #dae1e8;
    }
  }
}

</style>