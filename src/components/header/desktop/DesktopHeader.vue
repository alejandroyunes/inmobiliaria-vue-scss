<script lang="ts" setup>
import './desktop-header.scss'
import { ref } from 'vue'
import Menu from './menu/MenuComponent.vue'
import RightNav from '@/components/sliders/right-nav/RightNav.vue'
import SunSvg from '@/components/icons/header/SunSvg.vue'
import MoonSvg from '@/components/icons/header/MoonSvg.vue'
import HamburgerVerticalSvg from '@/components/icons/header/HamburgerVerticalSvg.vue'

interface Props {
  isDarkMode: boolean
  handleTheme: () => void
}

const { isDarkMode, handleTheme } = defineProps<Props>()
const isRightNavOpen = ref<boolean | undefined>(undefined)

const toggleRightNav = () => {
  isRightNavOpen.value = !isRightNavOpen.value
}

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
        <HamburgerVerticalSvg @click="toggleRightNav" class="icon" />
        <RightNav :toggleRightNav="toggleRightNav" :isRightNavOpen="isRightNavOpen" />
      </div>
    </div>

  </nav>
</template>