<script setup lang="ts">

</script>

<template>
  <div>
    <ClientOnly fallback-tag="span">
      <!-- this component will only be rendered on client side -->
      <QrCodeScanner />
      <template #fallback>
        <!-- this will be rendered on server side -->
        <p>Loading comments...</p>
      </template>
    </ClientOnly>
  </div>
</template>
