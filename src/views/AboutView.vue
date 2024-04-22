<script lang="ts" setup>
import ImageHeader from '@/components/sections/01-row/image-header/ImageHeader.vue'
import MissionVision from '@/components/sections/02-row/mission-vision/MissionVision.vue'
</script>

<template>
  <ImageHeader :imageUrl="'/images/sections/01-row/title-header/about.webp'"  :title="'About us'" />
  <MissionVision />
</template>