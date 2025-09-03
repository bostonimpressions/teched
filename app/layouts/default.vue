<script setup lang="ts">
  useHead({
    title:
      'Career and Technical Education Training | TechEd Products | United States',
    meta: [
      {
        name: 'description',
        content:
          'With over 50 years combined experience serving New England, TechEd Products is the area’s most experienced independent educational sales consultant organization.',
      },
      {
        property: 'og:title',
        content:
          'Career and Technical Education Training | TechEd Products | United States',
      },
      {
        property: 'og:description',
        content:
          'With over 50 years combined experience serving New England, we are the area’s most experienced independent educational sales consultant organization. By combining our local knowledge and relationships with our partners, we provide the best solutions to prepare your students or trainees with critical STEM and job ready skills required in today’s technical workforce.',
      },
    ],
    link: [
      {
        rel: 'canonical',
        href: 'https://www.techedproducts.com',
      },
    ],
  })
</script>

<template>
  <main>
    <slot />
  </main>
  <BaseFooter />
</template>
