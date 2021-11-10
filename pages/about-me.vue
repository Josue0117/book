<template>
  <div class="content">
    <NavBar />
    <div class="row">
      <div class="col-4 hero-image">
        <img :src="require('@/assets/images/hero-image.png')" alt="hero-image">
      </div>
    </div>
    <Footer />
  </div>
</template>

<style scoped>
.content {
  height: 100%;
}

.row {
  width: 100%;
  height: 100%;
}

.hero-image img {
  border-radius: 50%;
box-shadow: 0 0 15px #938e7e;
  margin-top: 15%;
  margin-left: 25%;
  width: 70%;
}
</style>
