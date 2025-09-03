<script setup lang="ts"></script>

<template>
  <div class="hero">
    <div class="container">
      <BaseHeader />
    </div>
    <div class="container hero-container">
      <slot />
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

  .hero-container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    flex: 1;
    gap: 20px;
    text-align: center;
    max-width: 1047px;
    padding: 30px 20px;
    margin: 0 auto;
    color: var(--white);
    :deep(p) {
      color: var(--white);
    }
  }

  @media (min-width: 1048px) {
    .hero-container {
      padding: 0;
    }
  }
</style>
