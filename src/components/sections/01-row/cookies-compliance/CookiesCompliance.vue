<script setup lang="ts">
import './cookies-compliance.scss'

const { handleCookies } = defineProps<{ handleCookies: () => void }>()
</script>

<template>
  <div class="cookies-compliance-outer">
    <p class="cookies-compliance-text">We use cookies to improve user experience and analyze website traffic. For
      these reasons, we may share your site usage data with our analytics partners. By continuing to the site, you
      consent to store on your device all the technologies described in our terms and conditions.</p>
    <button class="cookies-compliance-button" @click="handleCookies">
      Ok
    </button>
  </div>
</template>