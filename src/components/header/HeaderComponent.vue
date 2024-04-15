<script lang="ts" setup>
import { ref } from 'vue'

import { setDarkMode } from '@/utils/utils'

const isDarkMode = ref<boolean>(localStorage.getItem('isDarkMode') === 'true')
setDarkMode(isDarkMode.value)

const handleTheme = () => {
  isDarkMode.value = !isDarkMode.value
  setDarkMode(isDarkMode.value)
}


</script>

<template>
  <nav class="outer">

  </nav>
</template>


