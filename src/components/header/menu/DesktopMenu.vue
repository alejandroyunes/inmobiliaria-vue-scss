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

    <div class="left">
      <router-link to="/" class="link">
        <p class="capital">
          Estrella <span class="invest">Immobilien GmbH</span>
        </p>
      </router-link>
      <div>
        hello
      </div>
    </div>

    <div class="right">
      <div>hello</div>
      <div>good bye</div>
    </div>
      
  </nav>
</template>

<style lang="scss" scoped>
.outer {
  outline: 1px solid red;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  max-width: 1280px;
  margin: 0 auto;
}

.link {
  text-decoration: none;
  color: inherit;
}

.capital {
  font-size: 24px;
}

.invest {
  margin-right: 10px;
  font-size: 24px;
  color: #f1c40f;
  font-weight: bold;
}

.left {
  display: flex;
  align-items: center;
}

.right {
  display: flex;
  align-items: center;
}
</style>
