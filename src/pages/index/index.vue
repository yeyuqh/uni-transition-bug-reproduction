<script setup>
import { ref } from 'vue'

const show = ref(false)
</script>

<template>
  <view>
    <view style="display: flex; justify-content: center; align-items: center; width: 100vw; height: 100vh;">
      <button style="width: 100px;" @click="show = !show">SHOW</button>
    </view>

    <uni-transition
    :show="show" mode-class="fade" :duration="1000"
      :styles="{
        position: 'fixed',
        left: 0,
        right: 0,
        bottom: 0,
        zIndex: 900,
        width: '100vw',
        height: '100vh',
        backgroundColor: 'rgba(0, 0, 0, 0.8)',
      }"
    >
      <view style="display: flex; justify-content: center; align-items: center; width: 100vw; height: 100vh;">
        <button style="width: 100px; background-color: orange;" @click="show = !show">HIDE</button>
      </view>
    </uni-transition>
  </view>
</template>
