<template>
  <div>
    <div class="container-cards-roulete">
      <div class="cards-roulete">
        <InfoCard class="info-card card-1" />
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
  /* background-color: rgb(0, 0, 0); */
  width: 40%;
  height: 100%;
}

.info-card {
  animation: rigth-to-left 21s linear infinite;
}

.info-card.card-2{
  top: -300px;
  animation-delay: 7s;
}

.info-card.card-3{
  top: -750px;
  animation-delay: 14s;
}

@keyframes rigth-to-left {
  0% {
    transform: scale(100%);
    z-index: 4;
  }

  12.5% {
    transform: translateX(27%) scale(109%);
    z-index: 6;
  }

  25% {
    transform: translateX(50%) scale(115%);
  }

  37.5% {
    transform: translateX(73%) scale(109%);
    z-index: 5;
  }

  50% {
    transform: translateX(100%) scale(100%);
    z-index: 3;
  }

  75% {
    transform: translateX(50%) scale(85%);
  }
}
</style>
