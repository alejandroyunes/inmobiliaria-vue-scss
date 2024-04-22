<script lang="ts" setup>
import './title-arrow.scss'
import ArrowDownSvg from "@/components/icons/ArrowDownSvg.vue"

const { title } = defineProps<{
  title: string
}>()

</script>

<template>
  <section>
    <div class="title-arrow-container">
      <div class="title">
        <p>{{ title }}</p>
      </div>
      <div class="arrow">
        <ArrowDownSvg class="icon" />
      </div>
    </div>
  </section>
</template>
