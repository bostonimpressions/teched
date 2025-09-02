<script setup lang="ts"></script>

<template>
  <div class="hero">
    <div class="container">
      <BaseHeader />
    </div>
    <div class="container hero-container">
      <div class="hero-row">
        <div class="hero-content"></div>
      </div>
    </div>

    <div class="container brands">
      <!-- <LogoSlider class="logo-slider" /> -->
    </div>
  </div>
</template>

<style scoped lang="scss">
  .hero {
    background-color: var(--blue);
    background-image: url('/hero-bg.jpg');
    background-size: cover;
    background-position: center;
    min-height: 45vh;
    display: flex;
    flex-direction: column;
    padding: 60px 0 0;
  }
  .hero-row {
    display: flex;
    position: relative;
    flex: 1;
    padding: 40px 0;
    //align-items: center;
  }

  .hero-content {
    max-width: 605px;
    display: flex;
    flex-direction: column;
    //justify-content: center;
    align-items: flex-start;
    gap: 27px;
    color: white;
    &.dark {
      color: var(--blue);

      .content {
        color: var(--black);
      }
    }

    .logo {
      width: 283px;
      height: 54.017px;
      aspect-ratio: 241/46;
    }

    .category {
      font-size: 24px;
      font-style: italic;
      font-weight: 700;
      line-height: 30px;
    }

    .content {
      font-size: 18px;
      font-style: normal;
      font-weight: 400;
      line-height: 24px;
    }
  }

  .hero-container {
    display: flex;
    flex-direction: column;
    flex: 1;
  }

  .brands {
    position: relative;
    bottom: -48px;
  }

  /* Fade animation */
  .fade-enter-active,
  .fade-leave-active {
    transition: opacity 1s;
  }
  .fade-enter-from,
  .fade-leave-to {
    opacity: 0;
  }
</style>
