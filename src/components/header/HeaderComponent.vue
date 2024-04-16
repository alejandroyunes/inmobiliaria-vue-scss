<script lang="ts" setup>
import './header-component.scss'
import { ref } from 'vue'

import { setDarkMode } from '@/utils/utils'
import Desktop from './desktop/DesktopComponent.vue'
import Mobile from './mobile/MobileComponent.vue'

const isDarkMode = ref(localStorage.getItem('isDarkMode') === 'true')
setDarkMode(isDarkMode.value)

const handleTheme = () => {
  isDarkMode.value = !isDarkMode.value
  setDarkMode(isDarkMode.value)
}

</script>

<template>

  <div class="desktop">
    <Desktop :handleTheme="handleTheme" :isDarkMode="isDarkMode" />
  </div>

  <div class="mobile">
    <Mobile />
  </div>

</template>

<style lang="scss" scoped></style>
