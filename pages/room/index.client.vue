<script setup lang="ts">
import QrScanner from 'qr-scanner'

const video = ref<HTMLVideoElement>()

onMounted(() => {
  const scanner = new QrScanner(
    video.value!,
    (result) => {
      // console.log('QR code detected:', result.data)
      if (result.data.startsWith(window.location.hostname))
        window.location.href = result.data
    },
    {
      highlightScanRegion: true,
      highlightCodeOutline: true,
      returnDetailedScanResult: true,
    },
  )

  scanner.start()
})
</script>

<template>
  <div>
    <video ref="video" class="object-fill" />
  </div>
</template>
