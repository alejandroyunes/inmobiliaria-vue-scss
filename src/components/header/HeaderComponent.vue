<script lang="ts" setup>
import { ref } from 'vue'

import { setDarkMode } from '@/utils/utils'
import Desktop from './desktop/DesktopHeader.vue'

const isDarkMode = ref(localStorage.getItem('isDarkMode') === 'true')
setDarkMode(isDarkMode.value)

const handleTheme = () => {
  isDarkMode.value = !isDarkMode.value
  setDarkMode(isDarkMode.value)
}

</script>

<template>
  <Desktop :handleTheme="handleTheme" :isDarkMode="isDarkMode" />
</template>

<style lang="scss" scoped></style>
