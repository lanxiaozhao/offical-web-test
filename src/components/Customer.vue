<template>
<div class="customer">
  <p class="customer__head">Join thousands of designers at world’s leading companies who use Gifmock to create high-quality GIFs.</p>
  <div class="customer__logo">
    <customer-svg></customer-svg>
  </div>
</div>
</template>

<script lang='ts' setup>
import CustomerSvg from './customerSvg.vue'

</script>

<style lang='less' scoped>
.customer {
  padding: 80px 0 160px;
  &__head {
    font-size: 30px;
    line-height: 1.4em;
    font-weight: 400;
    margin: 0;
    padding: 0;
    color: #dae1e8;
    max-width: 800px;
    margin: 0 auto;
    text-align: center;
  }
  &__logo {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    margin-top: 24px;
    align-items: center;
  }
}

</style>