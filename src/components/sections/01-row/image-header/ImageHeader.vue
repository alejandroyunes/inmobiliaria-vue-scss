<script lang="ts" setup>
import './image-header.scss'

interface ImageHeaderProps {
  imageUrl: string
  title: string
  marginTop?: boolean
}

const { imageUrl, title } = defineProps<ImageHeaderProps>()

</script>

<template>
  <section>
    <div class="title-header-container">
      <div class="position" :class="{'margin-top': marginTop}">
        <img class="image" :src="imageUrl" alt="alt" width="1280px" height="360px" />
        <div class="bg-overlay"></div>
        <div class="center-text">
          <p class="text">{{ title }}</p>
        </div>
      </div>
    </div>
  </section>
</template>
