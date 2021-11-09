<template>
  <div class="content">
    <p class="footer-block-tittle">{{ title }}</p>
    <p v-for="value in values" v-bind:key="value" class="footer-block-value">
      {{ value }}
    </p>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: '',
    },
    values: {
      type: Array,
      default: [],
    },
  },
}
</script>

<style scoped>
p {
  margin-bottom: 0;
}

p.footer-block-tittle {
  color: #01a4ff;
}

p.footer-block-value {
  color: white;
}
</style>
