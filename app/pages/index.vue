<script setup lang="ts">
  // const { data: intro } = await useAsyncData(() =>
  //   queryCollection('content').path('/home/intro').first()
  // )
</script>

<template>
  <Hero>
    <h1>Your Local Partner in Education & Industry Solutions</h1>
    <p>
      We provide comprehensive support for all your curriculum, equipment,
      eLearning, and professional development needs—tailored for both
      educational institutions and industry professionals.
    </p>

    <Brands />
  </Hero>
  <SectionProducts />
</template>

<style lang="scss" scoped>
  @media (min-width: 768px) {
    .test {
      color: red;
    }
  }
</style>
