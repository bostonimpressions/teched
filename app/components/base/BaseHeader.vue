<script setup>
  import { ref, onMounted, onBeforeUnmount } from 'vue'
  const isOpen = ref(false)

  const links = [
    { name: 'Home', url: `/` },
    { name: 'Programs', url: `programs` },
    { name: 'Who We Are', url: `who-we-are` },
    { name: 'Contact Us', url: `contact-us` },
  ]

  const handleClickOutside = (event) => {
    const nav = document.querySelector('.navigation')
    const hamburger = document.querySelector('.hamburger')
    if (
      isOpen.value &&
      !nav.contains(event.target) &&
      !hamburger.contains(event.target)
    ) {
      isOpen.value = false
    }
  }

  const handleEsc = (event) => {
    if (isOpen.value && event.key === 'Escape') {
      isOpen.value = false
    }
  }

  onMounted(() => {
    window.addEventListener('click', handleClickOutside)
    window.addEventListener('keydown', handleEsc)
  })

  onBeforeUnmount(() => {
    window.removeEventListener('click', handleClickOutside)
    window.removeEventListener('keydown', handleEsc)
  })
</script>

<template>
  <header class="base-header">
    <div class="branding">
      <BaseLogo />
    </div>

    <button
      class="hamburger"
      @click="isOpen = !isOpen"
      aria-label="Toggle Menu"
      :class="{ open: isOpen }"
    >
      <span class="line"></span>
      <span class="line"></span>
      <span class="line"></span>
    </button>

    <!-- nav -->
    <nav class="navigation" :class="{ open: isOpen }">
      <ul>
        <li v-for="link in links" :key="link.url">
          <NuxtLink :to="link.url">{{ link.name }}</NuxtLink>
        </li>
      </ul>

      <!-- Mobile socials -->
      <div class="mobile-socials">
        <BaseSocials />
      </div>
    </nav>

    <!-- Desktop socials -->
    <div class="desktop-socials">
      <BaseSocials dark />
    </div>
  </header>
</template>

<style lang="scss" scoped>
  .base-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    color: var(--black);
    padding: 22px 60px;
    border-radius: 10px;
    background: #fff;
    box-shadow: 0 6px 20px 0 rgba(0, 0, 0, 0.1);
  }

  .hamburger {
    display: none;
    flex-direction: column;
    justify-content: space-between;
    width: 24px;
    height: 18px;
    background: none;
    border: none;
    cursor: pointer;
    z-index: 3;

    .line {
      display: block;
      height: 3px;
      width: 100%;
      background: var(--black);
      border-radius: 2px;
      transition: 0.3s ease;
    }

    &.open {
      .line {
        background: var(--white);

        &:nth-child(2) {
          opacity: 0;
        }
        &:nth-child(1) {
          transform: translateY(7px) rotate(45deg);
        }
        &:nth-child(3) {
          transform: translateY(-8px) rotate(-45deg);
        }
      }
    }
  }

  .navigation {
    display: flex;
    flex-direction: row;
    align-items: end;
    gap: 60px;
  }

  ul {
    display: flex;
    flex-direction: row;
    gap: 50px;
    list-style: none;
    margin: 0;
    padding: 0;

    li {
      display: flex;
      flex-direction: row;
      cursor: pointer;
    }

    a {
      cursor: pointer;
    }
  }

  .desktop-socials {
    display: flex;
  }

  .mobile-socials {
    display: none;
  }

  @media (max-width: 1024px) {
    .base-header {
      padding: 22px;
    }
    .navigation {
      position: fixed;
      top: 0;
      right: 0;
      height: 100vh;
      width: 300px;
      background: var(--black);
      color: var(--white);
      flex-direction: column;
      transform: translateX(100%);
      transition: transform 0.3s ease;
      padding: 2rem;
      z-index: 2;

      &.open {
        transform: translateX(0);
      }

      font-size: 16px;
      align-items: flex-start;

      ul {
        flex-direction: column;
        gap: 20px;
        padding-top: 150px;
      }
    }

    .desktop-socials {
      display: none;
    }

    .mobile-socials {
      display: flex;
      margin-top: 40px;
    }

    .hamburger {
      display: flex;
    }

    .nav-top,
    .nav-bottom {
      padding: 20px 0;
    }
  }
</style>
