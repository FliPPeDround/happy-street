<script setup lang="ts">
import { StyleProvider, Themes } from '@varlet/ui'
import { appName } from '~/constants'

useHead({
  title: appName,
})
StyleProvider(Themes.md3Dark)
</script>

<template>
  <VitePwaManifest />
  <NuxtLayout>
    <NuxtPage />
  </NuxtLayout>
</template>

<style>
html,
body,
#__nuxt {
  height: 100vh;
  margin: 0;
  padding: 0;
}

html {
  @apply bg-body;
}
</style>
