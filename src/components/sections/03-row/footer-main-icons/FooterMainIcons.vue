<script lang="ts" setup>
import './footer-main-icons.scss'
import ClockSvg from "@/components/icons/contact/ClockSvg.vue"
import Phone from "@/components/icons/contact/PhoneSvg.vue"
import MapSvg from "@/components/icons/contact/MapSvg.vue"

</script>

<template>
  <section>
    <div class="footer-main-icons">

      <div>
        <div class="svg">
          <ClockSvg />
        </div>
        <p>Mon - Fri: 9 AM – 22 PM</p>
        <p>Saturday: 9 AM – 20 PM</p>
        <p>Sunday: Closed</p>
      </div>

      <div>
        <div class="svg">
          <MapSvg />
        </div>
        <p>Grützenstrasse 18807 FreienbachSchweiz</p>
      </div>

      <div>
        <div class="svg">
          <Phone />
        </div>
        <a class="tel" href="tel:+41787746337">+41 78 774 63 37</a>
        <a class="email" href="mailto:matthias.schulz@estrella-immobilien.ch">matthias.schulz@estrella-immobilien.ch</a>
      </div>

    </div>

  </section>
</template>
