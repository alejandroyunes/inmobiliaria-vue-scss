<script lang="ts" setup>
import './desktop-header.scss'
import { ref } from 'vue'
import Menu from './menu/MenuComponent.vue'
import RightNav from '@/components/sliders/right-nav/RightNav.vue'
import SunSvg from '@/components/icons/header/SunSvg.vue'
import MoonSvg from '@/components/icons/header/MoonSvg.vue'
import HamburgerVerticalSvg from '@/components/icons/header/HamburgerVerticalSvg.vue'
import HamburgerMenu from '@/components/icons/header/HamburgerSvg.vue'

interface Props {
  isDarkMode: boolean
  handleTheme: () => void
}

const { isDarkMode, handleTheme } = defineProps<Props>()
const isRightNavOpen = ref<boolean | undefined>(undefined)
const isMobileMenuOpen = ref<boolean | undefined>(undefined)

const toggleRightNav = () => {
  isRightNavOpen.value = !isRightNavOpen.value
}

const handleMobileMenu = () => {
  isMobileMenuOpen.value = !isMobileMenuOpen.value
}

</script>

<template>
  <nav class="desktop-container">
    <div class="left">
      <HamburgerMenu :handleMobileMenu="handleMobileMenu" class="icon mobile-only hamburger" />
      <TopNav :handleMobileMenu="handleMobileMenu" :isMobileMenuOpen="isMobileMenuOpen" />
      <router-link to="/" class="link">
        <span class="capital">Estrella</span>
        <span class="invest">Immobilien</span>
        <span class="invest desktop-only">GmbH</span>
      </router-link>
      <div>
        <Menu class="desktop-only" />
      </div>
    </div>

    <div class="right">
      <div class="dark-mode-icons">
        <MoonSvg v-show="!isDarkMode" @click="handleTheme" class="icon sun" />
        <SunSvg v-show="isDarkMode" @click="handleTheme" class="icon moon" />
      </div>
      <div>
        <HamburgerVerticalSvg @click="toggleRightNav" class="icon desktop-only" />
        <RightNav :toggleRightNav="toggleRightNav" :isRightNavOpen="isRightNavOpen" />
      </div>
    </div>

  </nav>
</template>