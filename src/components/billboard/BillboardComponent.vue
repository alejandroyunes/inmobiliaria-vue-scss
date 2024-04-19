<script lang="ts" setup>
import './billboard-component.scss'
import ArrowDownSvg from '../icons/ArrowDownSvg.vue';
</script>

<template>
  <section class="billboard-container">
    <div class="billboard-left">
      <div class="billboard-title">
        <div class="slogan">
          <h3>Seamless booking and property management</h3>
        </div>
        <div>
          <h1 class="title">Luxury Stays &</h1>
          <h1 class="title">Management</h1>
          <h1 class="title">Rentals</h1>
        </div>
        
        <router-link to="/about">
          <button class="action-button">Explore</button>
        </router-link>
      </div>
      <div class="billboard-arrow">
        <div class="arrow-rotate">
          <div class="arrow">
            <ArrowDownSvg class="icon" />
          </div>
        </div>
      </div>
    </div>

    <div class="billboard-right">
      <img class="billboard-image" src="/images/billboard/home-billboard.webp" alt="alt" />
      <div class="image-bg" />
    </div>

  </section>
</template>
