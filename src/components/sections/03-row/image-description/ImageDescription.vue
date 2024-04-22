<script lang="ts" setup>
import './image-description.scss'
</script>

<template>
  <section>
    <div class="image-description-container">

      <div class="item">
        <img class="image" src="/images/sections/main-three-images/service1.webp" alt="Real Estate" />
        <p class="title">Real Estate</p>
        <h3>Real estate with tailored solutions for your property.</h3>
      </div>

      <div class="item">
        <img class="image" src="/images/sections/main-three-images/management.webp" alt="Management" />
        <p class="title">Management</p>
        <h3>Effortless property management.</h3>

      </div>
      <div class="item">
        <img class="image" src="/images/sections/main-three-images/construction.webp" alt="Construction" />
        <p class="title">Construction</p>
        <h3>Supporting construction projects with expertise.</h3>
      </div>
    </div>

    <div class="image-description-button">
      <router-link to="/services">
        <button>Services</button>
      </router-link>
    </div>

  </section>
</template>
