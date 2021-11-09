<template>
  <footer>
    <div class="title">
      <div>
        <p class="footer-title">{{ navBarTitle }}</p>
        <p class="footer-subtitle">{{ navBarSubtitle }}</p>
      </div>
    </div>
    <div class="contact">
      Correos
    </div>
  </footer>
</template>

<script>
import { CARD_1_TITLE, CARD_1_SUBTITLE } from '@/constants-static-texts.js'
export default {
  data: () => {
    return {
      navBarTitle: CARD_1_TITLE.toUpperCase(),
      navBarSubtitle: CARD_1_SUBTITLE.toUpperCase(),
    }
  }
}
</script>

<style scoped>
footer {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: #00071F;
}

.title {
  padding: 25px;
  text-align: left;
  background: linear-gradient(180deg, #00071F 0%, #000000 100%);
}

.title div {
  width: auto;
  margin-left: 2%;
  text-align: center;
}

p.footer-title {
  color: white;
  margin-bottom: 0;
}

p.footer-subtitle {
  color: #01A4FF;
  font-size: 12px;
  margin-bottom: 0;
}
</style>
