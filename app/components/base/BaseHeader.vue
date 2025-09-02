<script setup>
  import { ref } from 'vue'
  const isOpen = ref(false)
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
      :class="isOpen ? 'open' : null"
    >
      <span></span>
      <span></span>
      <span></span>
    </button>

    <!-- nav -->
    <nav class="navigation" :class="{ open: isOpen }">
      <ul>
        <li>im a link</li>
      </ul>
    </nav>
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
    z-index: 1001; // keeps button above menu

    span {
      display: block;
      height: 3px;
      width: 100%;
      background: var(--white);
      border-radius: 2px;
      transition: 0.3s ease;
    }
  }
  .navigation {
    display: flex;
    flex-direction: column;
    align-items: end;

    @media (max-width: 768px) {
      position: fixed;
      top: 0;
      right: 0;
      height: 100vh;
      width: 300px;
      background: #111;
      flex-direction: column;
      transform: translateX(100%);
      transition: transform 0.3s ease;
      padding: 2rem;
      z-index: 1000;

      &.open {
        transform: translateX(0);
      }

      nav {
        ul {
          flex-direction: column;
          gap: 20px;
        }
      }
    }
  }
  ul {
    display: flex;
    flex-direction: row;
    gap: 26px;
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
  .nav-top {
    display: flex;
    justify-self: flex-end;
    font-size: 16px;

    .icon {
      margin: 0 10px 0 0;
    }
    .special {
      color: var(--lightorange);
    }
  }
  .nav-bottom {
    display: flex;
    justify-self: flex-end;
    padding: 50px 0;
    font-size: 18px;
    ul {
      gap: 32px;
    }
    .text {
      display: flex;
      flex-direction: row;
      align-items: center;
    }
    .icon-caret {
      margin: 0 0 0 8px;
    }
  }
  @media (max-width: 768px) {
    .navigation {
      align-items: flex-start;
    }

    .hamburger {
      display: flex;

      &:not(.open) {
        span {
          background-color: var(--black);
        }
      }
    }

    .nav-top,
    .nav-bottom {
      padding: 20px 0;
    }
  }
</style>
