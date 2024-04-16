<script lang="ts" setup>
import './header-component.scss'
import { ref } from 'vue'

import { setDarkMode } from '@/utils/utils'
import DesktopMenu from './menu/DesktopMenu.vue';

const isDarkMode = ref<boolean>(localStorage.getItem('isDarkMode') === 'true')
setDarkMode(isDarkMode.value)

const handleTheme = () => {
  isDarkMode.value = !isDarkMode.value
  setDarkMode(isDarkMode.value)
}

</script>

<template>

  <div class="desktop">
    <DesktopMenu />
  </div>

  <div class="mobile">
    mobile
  </div>

</template>

<style lang="scss" scoped>

</style>
