<template>
<!-- <div class="select">
  <div class="select-item" :class="{'select-item--active': selected === 'month'}" @click="change('month')">Monthly</div>
  <div class="select-item" :class="{'select-item--active': selected === 'year'}" @click="change('year')">Yearly</div>
</div> -->
<div class="price">
  <!-- <div class="price-item">
    <div class="type">STARTER</div>
    <div class="amount">Free</div>
    <div class="note">No credit card required, no trial period</div>
    <div class="feature">
      <div class="feature-item">Crop tool</div>
      <div class="feature-item">Crop tool</div>
      <div class="feature-item">Crop tool</div>
      <div class="feature-item">Crop tool</div>
    </div>
    <div class="icon">
      <div class="icon-item">
        <img :src="`/src/assets/icon/fengche.svg`" alt="icon">
      </div>
      <div class="icon-item">
        <img :src="`/src/assets/icon/fengche.svg`" alt="icon">
      </div>
      <div class="icon-item">
        <img :src="`/src/assets/icon/fengche.svg`" alt="icon">
      </div>
    </div>
  </div> -->
  <div class="price-item">
    <div class="type">PRO</div>
    <div class="amount">{{amount}}<span class="unit">USD</span></div>
    <div class="note">{{amountInfo}}</div>
    <div class="feature">
      <div class="feature-item">Crop tool</div>
      <div class="feature-item">Crop tool</div>
      <div class="feature-item">Crop tool</div>
      <div class="feature-item">Crop tool</div>
    </div>
    <div class="icon">
      <button class="btn btn__middle">Sing Up</button>
    </div>
  </div>
  <div class="price-item">
    <div class="type">COMPANY</div>
    <div class="amount">{{amount}}<span class="unit">USD</span></div>
    <div class="note">For teams of 9+ people</div>
    <div class="feature">
      <div class="feature-item">Crop tool</div>
      <div class="feature-item">Crop tool</div>
      <div class="feature-item">Crop tool</div>
      <div class="feature-item">Crop tool</div>
    </div>
    <div class="icon">
      <button class="btn btn__last">Contact us</button>
    </div>
  </div>
</div>
</template>

<script lang='ts' setup>
import { ref } from 'vue'
// const selected = ref('month')
const amount = ref('$5')
const amountInfo = ref('Per user per month. Pay yearly & save $10')
// const change = (val: string) => {
//   selected.value= val
//   if (val === 'month') {
//     amount.value = '$5'
//     amountInfo.value= 'Per user per month. Pay yearly & save $10'
//   } else {
//     amount.value = '$50'
//     amountInfo.value= 'Per user per year. Saving $10'
//   }
// }
</script>

<style lang='less' scoped>
.select {
  margin: 8px 0 0 8px;
  display: flex;
  align-items: center;
  padding: 32px 0 ;
  justify-content: center;
  &-item {
    margin: 0 16px;
    cursor: pointer;
    font-size: 18px;
    font-weight: 600;
    &:hover {
      color: #dae1e8;
    }
    &--active {
      border-bottom: 2px solid rgb(0, 235, 203);
      color: #dae1e8;
    }
  }
}
.price {
  margin: 8px 0;
  display: flex;
  justify-content: center;
  &-item {
    width: 340px;
    background: rgba(234,241,248,0.05);
    border-radius: 19px;
    padding: 32px;
    margin: 0 8px;
    .type {
      color: #00ebcb;
      text-transform: uppercase;
      font-size: 12px;
      font-weight: 600;
      letter-spacing: .06em;
    }
    .amount {
      font-size: 40px;
      font-weight: 600;
      color: #dae1e8;
      .unit {
        font-size: 12px;
        font-weight: 600;
        letter-spacing: .06em;
        margin-left: 4px;
      }
    }
    .note {
      font-size: 14px;
      font-weight: 600;
      color: #dae1e8;
    }
    .feature {
      margin-top: 24px;
      &-item {
        padding: 4px 0;
        font-size: 18px;
      }
    }
    .icon {
      display: flex;
      margin-top: 24px;
      &-item {
        flex: 1;
        margin-left: 16px;
        height: 48px;
        border-radius: 9px;
        background: rgba(234,241,248,0.05);
        display: flex;
        align-items: center;
        justify-content: center;
        cursor: pointer;
        &:first-of-type {
          margin-left: 0;
        }
        img {
          width: 24px;
          height: 24px;
        }
        &:hover {
          background: rgba(234,241,248,0.08);
          box-shadow: 0 0 0 1px rgba(0,0,0,0.08),0 12px 20px -8px rgba(0,0,0,0.5);
        }
      }
    }
    &:first-of-type {
      margin-left: 0;     
      .type {
        color: rgb(33, 148, 255);
      }
    }
    &:last-of-type {
      margin-right: 0;
    }
  }
}
.btn {
  height: 48px;
  padding: 0 24px 1px;
  font-size: 18px;
  border-radius: 9px;
  border: none;
  width: 100%;
  font-weight: 600;
  cursor: pointer;
  &__middle {
    background: #00ebcb;
    color: #000;
    &:hover {
      background: #49ebd5;
      box-shadow: 0px 12px 20px -8px rgba(0,0,0,0.8);
    }
  }
  &__last {
    background: rgba(234,241,248,0.05);
    color: #dae1e8;
    &:hover {
      background: rgba(234,241,248,0.08);
      box-shadow: 0 0 0 1px rgba(0,0,0,0.08),0 12px 20px -8px rgba(0,0,0,0.5);
    }
  }
}
</style>