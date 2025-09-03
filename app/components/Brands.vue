<script setup lang="ts">
  import { ref, onMounted, nextTick } from 'vue'

  const brands = [
    { name: 'Levil', img: '/logos/levil.png', url: '' },
    { name: 'Amatrol', img: '/logos/amatrol.png', url: '' },
    { name: 'Bayport', img: '/logos/bayport.png', url: '' },
    { name: 'DAC', img: '/logos/dac.png', url: '' },
    { name: 'BrainCo', img: '/logos/brainco.png', url: '' },
  ]

  const track = ref<HTMLElement | null>(null)
  const duration = ref(20) // will calculate based on width

  onMounted(() => {
    nextTick(() => {
      if (track.value) {
        const firstList = track.value.querySelector(
          '.brands-list'
        ) as HTMLElement
        if (firstList) {
          const listWidth = firstList.offsetWidth
          track.value.style.setProperty('--list-width', `${listWidth}px`)
          const speed = 50 // pixels per second
          duration.value = listWidth / speed
        }
      }
    })
  })
</script>

<template>
  <div class="brands-wrapper">
    <div
      class="brands-track"
      ref="track"
      :style="{ animationDuration: `${duration}s` }"
    >
      <div class="brands-list" v-for="copy in 2" :key="copy">
        <div
          v-for="brand in brands"
          :key="copy + brand.name"
          class="brand-item"
        >
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
    padding: 23px 20px;
    margin: 0 auto;
    width: 100%;
    max-width: 720px;

    .brands-track {
      display: flex;
      flex-wrap: nowrap;
      animation: scroll linear infinite;

      &:hover {
        animation-play-state: paused;
      }

      .brands-list {
        display: flex;
        gap: 52px;
        flex: 0 0 auto;

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
          flex: 0 0 0; // keeps natural gap
        }
      }
    }
  }

  @keyframes scroll {
    0% {
      transform: translateX(0);
    }
    100% {
      transform: translateX(calc(-1 * var(--list-width)));
    }
  }

  @media (max-width: 480px) {
    .brands-wrapper {
      padding: 16px 10px;

      .brands-list {
        gap: 24px;
      }
    }
  }
</style>
