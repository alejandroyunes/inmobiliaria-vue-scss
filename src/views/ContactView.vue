<script lang="ts" setup>
import TitleArrow from '@/components/sections/01-row/title-arrow/TitleArrow.vue'
import FooterMainIcons from '@/components/sections/03-row/footer-main-icons/FooterMainIcons.vue'
import ImageHeader from '@/components/sections/01-row/image-header/ImageHeader.vue'
import ParnersComponent from '@/components/sections/01-row/partners/PartnersComponent.vue'
</script>

<template>
  <TitleArrow :title="'Contact'" />
  <FooterMainIcons />
  <ImageHeader :imageUrl="'/images/contact/contact.webp'" :title="'Contact us today'" marginTop/>
  <ParnersComponent />
</template>