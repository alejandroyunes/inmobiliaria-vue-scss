<script lang="ts" setup>
import './desktop-header.scss'
import Menu from './menu/MenuComponent.vue'
import SunSvg from '@/icons/header/SunSvg.vue'
import MoonSvg from '@/icons/header/MoonSvg.vue'

interface Props {
  isDarkMode: boolean
  handleTheme: () => void
}

const { isDarkMode, handleTheme } = defineProps<Props>()

</script>

<template>
  <nav class="outer">
    <div class="left">
      <router-link to="/" class="link">
        <p class="capital">
          Estrella <span class="invest">Immobilien GmbH</span>
        </p>
      </router-link>
      <div>
        <Menu />
      </div>
    </div>

    <div class="right">
      <div class="dark-mode-icons">
        <MoonSvg v-show="!isDarkMode" @click="handleTheme" class="icon sun" />
        <SunSvg v-show="isDarkMode" @click="handleTheme" class="icon moon" />
      </div>
      <div>
        <p>hello</p>
      </div>
    </div>

  </nav>
</template>