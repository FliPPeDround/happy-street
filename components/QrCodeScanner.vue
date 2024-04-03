<script setup lang="ts">
import { Html5QrcodeScanner } from 'html5-qrcode'

onMounted(() => {
  const qrCodeScanner = new Html5QrcodeScanner(
    'qr-reader',
    {
      fps: 10,
      qrbox: {
        width: 250,
        height: 250,
      },
    },
    /* verbose= */false,
  )

  qrCodeScanner.render(
    (decodedText, decodedResult) => {
      // eslint-disable-next-line no-console
      console.log(decodedText, decodedResult)
    },
    (error) => {
      console.error(`扫描出错: ${error}`)
    },
  )
})
</script>

<template>
  <div>
    <div id="qr-reader" style="width: 300px; height: 300px;" />
  </div>
</template>
