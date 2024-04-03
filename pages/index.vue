<script setup lang="ts">
</script>

<template>
  <div
    w-full mt10
    flex="~ col md:row"
    items-center justify-center
    space="y-5 md:x-5 md:y-0"
  >
    <var-paper
      ripple
      :elevation="2" :width="200" :height="200"
      class="enter-btn"
      @click="$router.push('/room')"
    >
      加入房间
    </var-paper>
    <var-paper 
      class="enter-btn"
      :elevation="2" :width="200" :height="200" ripple
    >
      创建房间
    </var-paper>
  </div>
</template>

<style>
.enter-btn {
  @apply cursor-pointer flex items-center justify-center;
}
</style>
