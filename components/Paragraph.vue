<template>
  <div class="content">
    <div class="paragraph-title">{{ title }}</div>
    <div class="line"></div>
    <div class="paragraph-content">{{ content }}</div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: '',
    },
    title: {
      type: String,
      default: ''
    },
    content: {
      type: String,
      default: ''
    }
  },
}
</script>

<style scoped>
.content {
  text-align: left;
  padding: 10%;
  padding-bottom: 0;
}

.paragraph-title {
  color: #6B6666;
}

.paragraph-content {
  font-size: 12px;
  color: #6B6666;
}

.line {
  width: 100%;
  height: 2px;
  background-color: #01A4FF;
}
</style>