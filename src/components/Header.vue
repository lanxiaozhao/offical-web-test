<template>
<div class="header">
  <img src="@/assets/logo.png" alt="logo" class="header__img">
  <div class="header__pricing" @click="goPrice" :class="{'header__pricing--active': flag}">Princing</div>
</div>
</template>

<script lang='ts' setup>
import {ref, watch} from 'vue'
import { useRouter, useRoute } from 'vue-router'
  const router = useRouter()
  const route = useRoute()
  const goPrice = () => {
    router.push({
      name: 'Pricing'
    })
  }
  const flag = ref(false)
 watch(() => route.name, val => {
   flag.value = val === 'Pricing'
 }, {immediate:true})

</script>

<style lang='less' scoped>
.header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  
  &__img {
    width: 24px;
    height: 24px;
  }
  &__pricing {
    font-weight: 600;
    cursor: pointer;
    font-size: 14px;
    &:hover {
      color: #dae1e8;
    }
    &--active {
      color: #dae1e8;
      border-bottom: 2px solid #00ebcb;
    }
  }
}

</style>