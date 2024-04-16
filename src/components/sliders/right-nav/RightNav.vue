<script lang="ts" setup>
import './right-nav.scss'
import Facebook from '@/components/icons/social-media/FacebookSvg.vue'
import Instagram from '@/components/icons/social-media/InstagramSvg.vue'
import Twitter from '@/components/icons/social-media/TwitterSvg.vue'
import Youtube from '@/components/icons/social-media/YoutubeSvg.vue'
import ExitSvg from '@/components/icons/ExitSvg.vue'

interface Props {
  toggleRightNav: () => void
  isRightNavOpen: boolean | undefined
}

const { toggleRightNav } = defineProps<Props>()

const closeMenu = () => {
  toggleRightNav()
  setTimeout(() => {
  }, 700)
}

</script>

<template>

  <div :class="['container', isRightNavOpen ? 'slide-in' : '', isRightNavOpen === false ? 'slide-out' : '']">
    <div class="header">
      <p class="capital">Estrella <span class="invest">Immobilien</span></p>

      <div @click="closeMenu" class="animation-exit">
        <ExitSvg />
      </div>
    </div>

    <div class="content">
      <ul class="body">
        <li class="items">
          <span class="svg">
            <Facebook />
          </span>
          <p class="paragrah">Facebook</p>
        </li>
        <li class="items">
          <span class="svg">
            <Instagram />
          </span>
          <p class="paragrah">Instagram</p>
        </li>
        <li class="items">
          <span class="svg">
            <Twitter />
          </span>
          <p class="paragrah">Twitter</p>
        </li>
        <li class="items">
          <span class="svg">
            <Youtube />
          </span>
          <p class="paragrah">Youtube</p>
        </li>
      </ul>

      <div class="contact">
        <p class="contact-tel"><a href="tel:+41787746337">+41 78 774 63 37</a></p>
        <p class="contact-email"><a
            href="mailto:matthias.schulz@estrella-immobilien.ch">matthias.schulz@estrella-immobilien.ch</a></p>
      </div>
    </div>
  </div>

  <div v-if="isRightNavOpen" @click="toggleRightNav" class="bg"></div>
</template>