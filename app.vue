<script setup lang="ts">
import { Themes } from '@varlet/ui'
import { appName } from '~/constants'

useHead({
  title: appName,
})
</script>

<template>
  <VitePwaManifest />
  <var-style-provider :style-vars="Themes.md3Dark">
    <NuxtLayout>
      <NuxtPage />
    </NuxtLayout>
  </var-style-provider>
</template>

<style>
html,
body,
#__nuxt {
  @apply bg-#141218 c-white;
  height: 100vh;
  margin: 0;
  padding: 0;
}
</style>
