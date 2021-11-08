<template>
  <div class="container">
    <div class="row header">
      <div class="col-5 hero-image">
        <img v-bind:src="imageUrl" />
      </div>
      <div class="col-7 title">
        <p>Josué Hernández <span>Web Developer</span></p>
      </div>
    </div>
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
</template>

<script>
import { 
ABOUT_ME_TITLE,
ABOUT_ME_CONTENT,
VISION_TITLE,
VISION_CONTENT,
DOWNLOAD_BUTTON_TEXT
} from '@/constants-static-texts.js'
export default {
  props: {
    imageUrl: {
      type: String,
      default: '',
    },
  },
  data: () => {
    return {
      aboutMeTitle: ABOUT_ME_TITLE,
      aboutMeContent: ABOUT_ME_CONTENT,
      visionTitle: VISION_TITLE,
      visionContent: VISION_CONTENT,
      buttonText: DOWNLOAD_BUTTON_TEXT
    }
  }
}
</script>

<style scoped>
.container {
  position: relative;
  width: 50%;
  height: 450px;
  top: 150px;
  border: 0.5px solid #e4e4e4;
}

.header {
  background-color: #c4c4c4;
}

.hero-image img {
  position: relative;
  width:90%;
  padding-top: 10%;
}

.title {
  padding: 0;
  padding-right: 5%;
  line-height: 15px;
}

.title p {
  color: white;
  font-size: 20px;
  text-align: center;
  padding-top: 20%;
}

.title span {
  font-size: 15px;
  color: #01A4FF;
}

.red-button {
  margin: 10%;
  padding-top: 6px;
  padding-bottom: 6px;
  width: 100%;
  font-size: 14px;
  background-color: #7E0000;
  color: white;
  border-radius: 5px;
  border: none;
}
</style>
