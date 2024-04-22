<script lang="ts" setup>
import './menu-component.scss'
</script>

<template>
  <div class="menu">
    <ul class="menu-list">
      <li class="menu-item">
        <router-link to="/" class="link">
          <span class="menu-span">Home</span>
        </router-link>
      </li>
      <li class="menu-item">
        <router-link to="/about" class="link">
          <span class="menu-span">About</span>
        </router-link>
      </li>
      <li class="menu-item">
        <router-link to="/services" class="link">
          <span class="menu-span">Services</span>
        </router-link>
      </li>
      <li class="menu-item">
        <router-link to="/contact" class="link">
          <span class="menu-span">Contact</span>
        </router-link>
      </li>
    </ul>
  </div>
</template>
