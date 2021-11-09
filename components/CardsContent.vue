<template>
  <div class="content">
    <!-- CARD 1 -->
    <div class="card-1" v-if="cardNumber == 1">
      <div class="row">
        <Paragraph :title="aboutMeTitle" :content="aboutMeContent" />
      </div>
      <div class="row">
        <Paragraph :title="visionTitle" :content="visionContent" />
      </div>
      <div class="row">
        <button class="red-button">
          {{ buttonText }}
        </button>
      </div>
    </div>

    <!-- CARD 2 -->
    <div class="card-2" v-if="cardNumber == 2">
      <div class="row">
        <Paragraph :title="programmingLanguages" />
      </div>
      <div class="row languages-container">
        <div
          class="col-4 language-icon"
          v-bind:key="languagueUrl"
          v-for="languagueUrl in programmingLanguagesUrls"
        >
          <img :src="require('@/assets/images/'+languagueUrl+'.png')" :alt="languagueUrl+'-logo'">
        </div>
      </div>
      <div class="row">
        <Paragraph title="Frameworks" />
      </div>
    </div>

    <!-- CARD 3 -->
    <div class="card-2" v-if="cardNumber == 3">
      <div class="row">
        <Paragraph :title="proyectTittle" :content="proyectDescription" />
      </div>
      <div class="row proyect-img">
        <div class="col-2"></div>
        <img class="col-8" :src="require('@/assets/images/coronavirus-azul.png')" alt="virus-image">
      </div>
    </div>
  </div>
</template>

<script>
import { PROGRAMMING_LANGUAGUES_URLS } from '@/constants-urls.js'
import {
  ABOUT_ME_TITLE,
  ABOUT_ME_CONTENT,
  VISION_TITLE,
  VISION_CONTENT,
  DOWNLOAD_BUTTON_TEXT,
  SUBTITLE_1_CARD_2,
  FRAMEWORKS_TITLE,
  PANDEMIC_SIMULATOR_TITLE,
  PANDEMIC_SIMULATOR_DESCRIPTION
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
      visionTitle: VISION_TITLE,
      visionContent: VISION_CONTENT,
      buttonText: DOWNLOAD_BUTTON_TEXT,
      programmingLanguages: SUBTITLE_1_CARD_2,
      programmingLanguagesUrls: PROGRAMMING_LANGUAGUES_URLS,
      frameworksTitle: FRAMEWORKS_TITLE,
      proyectTittle: PANDEMIC_SIMULATOR_TITLE,
      proyectDescription: PANDEMIC_SIMULATOR_DESCRIPTION
    }
  },
}
</script>

<style scoped>
.red-button {
  margin: 10%;
  padding-top: 6px;
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
