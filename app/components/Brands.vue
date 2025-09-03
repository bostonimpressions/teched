<script setup lang="ts">
  const brands = [
    {
      name: 'Levil',
      img: '/logos/levil.png',
      url: '',
    },
    {
      name: 'Amatrol',
      img: '/logos/amatrol.png',
      url: '',
    },
    {
      name: 'Bayport',
      img: '/logos/bayport.png',
      url: '',
    },
    {
      name: 'DAC',
      img: '/logos/dac.png',
      url: '',
    },
    {
      name: 'BrainCo',
      img: '/logos/brainco.png',
      url: '',
    },
  ]
</script>

<template>
  <ul class="brands">
    <li v-for="brand in brands" :key="brand.name">
      <img :src="brand.img" :alt="brand.img" />
    </li>
  </ul>
</template>

<style scoped lang="scss">
  .brands {
    display: flex;
    flex-direction: row;
    align-items: center;
    gap: 52px;
    list-style: none;
    max-width: 720px;
    padding: 23px 41px;
    margin: 0 auto;
    border-radius: 19px;
    background: rgba(255, 255, 255, 0.2);
    img {
      max-height: 30px;
    }
  }
</style>
