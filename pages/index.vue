<template>
  <div>
    <div class="container-cards-roulete">
      <div class="cards-roulete">
        <InfoCard class="info-card card-1" :image-url="require('@/assets/images/hero-image.png')"/>
        <InfoCard class="info-card card-2" />
        <InfoCard class="info-card card-3"/>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style>
.container-cards-roulete {
  position: relative;
  height: 100px;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
}

.cards-roulete {
  margin-left: auto;
  margin-right: auto;
  text-align: center;
  max-width: 1060px;
  width: 40%;
  height: 100%;
}

.info-card {
  animation: rigth-to-left 18s linear infinite;
  background: white;
  margin: 0;
}

.info-card.card-2{
  top: -300px;
  animation-delay: 6s;
}

.info-card.card-3{
  top: -750px;
  animation-delay: 12s;
}

@keyframes rigth-to-left {
  0% {
    transform: translateX(0) scale(100%);
    z-index: 4;
  }

  6.25% {
    transform: translateX(5%) scale(105%);
  }

  12.5% {
    transform: translateX(15%) scale(110%);
    z-index: 6;
  }

  18.75% {
    transform: translateX(30%) scale(115%);
    z-index: 6;
  }

  25% {
    transform: translateX(50%) scale(120%);
  }

  31.25% {
    transform: translateX(70%) scale(116%);
  }

  37.5% {
    transform: translateX(85%) scale(113%);
    z-index: 5;
  }

  43.75% {
    transform: translateX(95%) scale(109%);
  }

  50% {
    transform: translateX(100%) scale(100%);
    z-index: 3;
  }

  56.25% {
    transform: translateX(90%) scale(95%);
  }

  75% {
    transform: translateX(50%) scale(85%);
  }
}
</style>
