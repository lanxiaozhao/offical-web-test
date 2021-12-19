<template>
<div class="banner">
  <div class="banner__img" >
    <div>这里有一张大大的宣传图,也可能是一个轮播图~ ,先用个图片吧</div>
  </div>
  
</div>
</template>

<script lang='ts' setup>


</script>

<style lang='less' scoped>
.banner {
  padding: 80px 0 150px;
  &__img {
    height: 500px;
    width: 100%;
    background-image: url('../assets/banner.jpg');
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    box-sizing: border-box;
  }
}

</style>