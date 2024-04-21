<script lang="ts" setup>
import "./get-in-touch.scss"
import MobileSvg from "@/components/icons/MobileSvg.vue"
import LocationSvg from "@/components/icons/LocationSvg.vue"
</script>

<template>
  <section class="get-in-touch-container">

    <div class="get-in-touch-left">
      <p class="slogan">Contact Us</p>
      <p class="title">Get in touch</p>
      <p class="description">Feel free to reach out to us for any inquiries or assistance. We are here to help you find
        the perfect
        accommodation for your needs. Contact us via email or give us a call. Our dedicated team looks forward to
        assisting you with any questions or reservations.</p>
    </div>

    <div class="get-in-touch-right">

      <div class="column">
        <div class="icon-bg">
          <LocationSvg class="icon" />
        </div>
        <div class="location-details">
          <p class="address">Address</p>
          <p class="details">Grützenstrasse 18807 FreienbachSchweiz</p>
        </div>
      </div>

      <div class="column">
        <div class="icon-bg">
          <MobileSvg class="icon" />
        </div>
        <div class="location-details">
          <p class="address">Contact</p>
          <a class="details" href="tel:+41787746337">+41 78 774 63 37</a>
          <a class="details"
            href="mailto:matthias.schulz@estrella-immobilien.ch">matthias.schulz@estrella-immobilien.ch</a>
        </div>
      </div>

    </div>

  </section>
</template>
