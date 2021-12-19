<template>
<div class="advantage">
  <div v-for="(item, index) in advantageList" :key="index" class="advantage-item">
    <img :src="`/src/assets/icon/${item.icon}.svg`" alt="icon" class="icon">
    <h2 class="title">{{item.title}}</h2>
    <p class="desc">{{item.text}}</p>
  </div>
</div>
</template>

<script lang='ts' setup>
const advantageList =[
  {
    icon: 'caihong',
    title: 'Smart cropping',
    text: 'Crop all your frames in a few clicks to highlight a specific part of your design.'
  },
  {
    icon: 'feibiao',
    title: 'Pixel preview',
    text: 'Pan and zoom on the canvas to position your frames with pixel precision.'
  },
  {
    icon: 'fengche',
    title: 'Measurement',
    text: 'Hold option to show distance from the edge when moving your frame.'
  },
  {
    icon: 'heiban',
    title: 'Retina support',
    text: 'You can import and export at the resolution you like. 1x, 2x, 3x, you decide.'
  },
  {
    icon: 'jiangbei',
    title: 'Smart cropping',
    text: 'Crop all your frames in a few clicks to highlight a specific part of your design.'
  },
  {
    icon: 'qiqiu',
    title: 'Smart cropping',
    text: 'Crop all your frames in a few clicks to highlight a specific part of your design.'
  },
  {
    icon: 'xiansu',
    title: 'Smart cropping',
    text: 'Crop all your frames in a few clicks to highlight a specific part of your design.'
  },
  {
    icon: 'youxiang',
    title: 'Smart cropping',
    text: 'Crop all your frames in a few clicks to highlight a specific part of your design.'
  }
]

</script>

<style lang='less' scoped>
.advantage {
  padding: 64px 0 120px;
  display: grid;
  grid-template-columns: repeat(4, 1fr) ;
  grid-template-rows: repeat(2, 1fr) ;
  grid-column-gap: 80px;
  grid-row-gap: 80px;
  &-item {
    .icon {
      width: 24px;
      height: 24px;
    }
    .title{
      margin: 12px 0;
      font-size: 18px;
      font-weight: 600;
      color: #dae1e8;
      line-height: 1.4em;
    }
    .desc {
      font-size: 14px;
      line-height: 1.4em;
      font-weight: 400;
      margin: 0;
    }
  }
}

</style>