<script setup lang="ts">
  const brands = [
    { name: 'Levil', img: '/logos/levil.png', url: '' },
    { name: 'Amatrol', img: '/logos/amatrol.png', url: '' },
    { name: 'Bayport', img: '/logos/bayport.png', url: '' },
    { name: 'DAC', img: '/logos/dac.png', url: '' },
    { name: 'BrainCo', img: '/logos/brainco.png', url: '' },
  ]
</script>

<template>
  <div class="brands-wrapper">
    <div class="brands-track">
      <div class="brands-list">
        <div v-for="brand in brands" :key="'a' + brand.name" class="brand-item">
          <img :src="brand.img" :alt="brand.name" />
        </div>
        <div class="spacer"></div>
      </div>
      <div class="brands-list">
        <div v-for="brand in brands" :key="'b' + brand.name" class="brand-item">
          <img :src="brand.img" :alt="brand.name" />
        </div>
        <div class="spacer"></div>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
  .brands-wrapper {
    overflow: hidden;
    border-radius: 19px;
    background: rgba(255, 255, 255, 0.2);
    padding: 23px 41px;
    margin: 0 auto;
    max-width: 720px;

    .brands-track {
      display: flex;
      width: max-content;
      animation: scrollBrands 20s linear infinite;

      &:hover {
        animation-play-state: paused;
      }

      .brands-list {
        display: flex;
        gap: 52px;

        .brand-item {
          flex: 0 0 auto;
          cursor: pointer;

          img {
            display: block;
            height: 30px;
            width: auto;
          }
        }

        .spacer {
          flex: 0 0 0;
        }
      }
    }
  }

  @keyframes scrollBrands {
    0% {
      transform: translateX(0);
    }
    100% {
      transform: translateX(-50%);
    }
  }
</style>
