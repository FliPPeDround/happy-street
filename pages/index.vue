<script setup lang="ts">
</script>

<template>
  <div w-full flex justify-center space-x-5>
    <div class="enter-btn" @click="$router.push('/room')">
      加入房间
    </div>
    <div class="enter-btn">
      创建房间
    </div>
  </div>
</template>

<style>
.enter-btn {
  @apply bg-dark-3 p20 hover:bg-dark-1 cursor-pointer;
}
</style>
