<script setup lang="ts">
  import { Swiper, SwiperSlide } from 'swiper/vue'
  import { Navigation } from 'swiper/modules'
  import 'swiper/css'
  import 'swiper/css/navigation'

  const slides = [
    {
      name: 'K-12 Stem',
      img: '/stem.jpg',
      url: '',
    },
    {
      name: `Career & Technical Education`,
      img: '/education.jpg',
      url: '',
    },
    {
      name: 'Industry Training',
      img: '/training.jpg',
      url: '',
    },
    {
      name: 'Corporate Learning',
      img: '/stem.jpg',
      url: '',
    },
    {
      name: 'Adult Upskilling',
      img: '/education.jpg',
      url: '',
    },
  ]
</script>

<template>
  <section class="section-product-videos">
    <div class="products-cta">
      <h4>Our Products In Action</h4>
      <p>
        Watch our skilled technicians and engineers in action, demonstrating the
        quality, precision, and dedication that goes into every step of our work
      </p>
    </div>
    <div class="three-col-grid">
      <div class="grid-item"></div>
      <div class="grid-item"></div>
      <div class="grid-item"></div>
    </div>
  </section>
</template>

<style scoped lang="scss">
  .section-product-videos {
    position: relative;
    padding: 60px;
    background: var(--white);
    overflow: hidden;

    .products-cta {
      position: relative;
      display: flex;
      flex-direction: column;
      gap: 20px;
      margin: 0 auto 50px;
      text-align: center;
      z-index: 1;

      h4 {
        color: var(--blue);
      }

      p {
        max-width: 970px;
        margin: 0 auto;
        font-size: 16px;
        color: var(--black);
      }
    }

    &::before,
    &::after {
      position: absolute;
      content: '';
      width: 660px;
      height: 660px;
      background: url('/halftone.png') no-repeat center center;
      background-size: contain;
      pointer-events: none;
      opacity: 0.22;
      z-index: 0;
    }

    &::before {
      top: -370px;
      right: -250px;
    }

    &::after {
      bottom: -370px;
      left: -250px;
    }
  }

  .three-col-grid {
    position: relative;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
    z-index: 1;

    .grid-item {
      background: black;
      width: 100%;
      height: 280px;
      border-radius: 20px;
    }
  }

  @media (min-width: 768px) {
    .section-product-videos {
      padding: 100px;
    }
  }
</style>
