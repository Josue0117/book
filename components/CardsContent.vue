<template>
  <div class="content">
    <!-- CARD 1 -->
    <div class="card-1" v-if="cardNumber == 1">
      <div class="row">
        <Paragraph
          :title="aboutMeTitle"
          :content-multi-paragraph="aboutMeContent"
          context="dynamic"
        />
      </div>
      <div class="row">
        <button class="red-button">
          {{ buttonText }}
        </button>
      </div>
    </div>

    <!-- CARD 2 -->
    <div class="card-2" v-if="cardNumber == 2">
      <Paragraph
        :title="languagesSection.title"
        :skills-list="languagesSection.values"
        context="dynamic"
      />
    </div>

    <!-- CARD 3 -->
    <div class="card-2" v-if="cardNumber == 3">
      <div class="row">
        <Paragraph
          :title="proyectTittle"
          :content="proyectDescription"
          context="dynamic"
        />
      </div>
      <div class="row proyect-img">
        <div class="col-2"></div>
        <img
          class="col-8"
          :src="require('@/assets/images/coronavirus-azul.png')"
          alt="virus-image"
        />
      </div>
    </div>
  </div>
</template>

<script>
import { PROGRAMMING_LANGUAGUES_URLS } from '@/constants-urls.js'
import {
  ABOUT_ME_TITLE,
  ABOUT_ME_CONTENT,
  DOWNLOAD_BUTTON_TEXT,
  LANGUAGES_SECTION,
  PANDEMIC_SIMULATOR_TITLE,
  PANDEMIC_SIMULATOR_CONTENT,
} from '@/constants-static-texts.js'
export default {
  props: {
    cardNumber: {
      Type: Number,
      default: 0,
    },
  },
  data: () => {
    return {
      aboutMeTitle: ABOUT_ME_TITLE,
      aboutMeContent: ABOUT_ME_CONTENT,
      buttonText: DOWNLOAD_BUTTON_TEXT,
      languagesSection: LANGUAGES_SECTION,
      programmingLanguagesUrls: PROGRAMMING_LANGUAGUES_URLS,
      proyectTittle: PANDEMIC_SIMULATOR_TITLE,
      proyectDescription: PANDEMIC_SIMULATOR_CONTENT,
    }
  },
}
</script>

<style scoped>
.red-button {
  margin: -0.5% 5% 5% 5%;
  padding-bottom: 6px;
  width: 100%;
  font-size: 14px;
  background-color: #7e0000;
  color: white;
  border-radius: 5px;
  border: none;
}

.languages-container {
  padding: 10%;
  padding-bottom: 0;
}

.language-icon img {
  width: 100%;
  margin-bottom: 10px;
}

.proyect-img img {
  width: 100%;
  padding: 10%;
}
</style>
