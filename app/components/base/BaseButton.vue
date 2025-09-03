<script setup lang="ts">
  import { computed } from 'vue'
  import { NuxtLink } from '#components'

  const props = defineProps<{
    to?: string
    link?: boolean
    arrow?: boolean
  }>()

  // Decide whether we render a <NuxtLink> or <button>
  const tag = computed(() => (props.to ? NuxtLink : 'button'))
</script>

<template>
  <component
    :is="tag"
    v-bind="to ? { to } : {}"
    class="base-button"
    :class="{
      'is-link': link,
      'is-arrow': arrow,
    }"
  >
    <slot />
    <span v-if="arrow" class="icon">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="31"
        height="16"
        viewBox="0 0 31 16"
        fill="none"
      >
        <path
          d="M29.85 8.42439C30.2405 8.03387 30.2405 7.4007 29.85 7.01018L23.486 0.646217C23.0955 0.255693 22.4623 0.255693 22.0718 0.646217C21.6813 1.03674 21.6813 1.66991 22.0718 2.06043L27.7286 7.71729L22.0718 13.3741C21.6813 13.7647 21.6813 14.3978 22.0718 14.7884C22.4623 15.1789 23.0955 15.1789 23.486 14.7884L29.85 8.42439ZM0 7.71729L0 8.71729L29.1429 8.71729L29.1429 7.71729L29.1429 6.71729L0 6.71729L0 7.71729Z"
          fill="#198FC4"
        />
      </svg>
    </span>
  </component>
</template>

<style scoped lang="scss">
  @use 'sass:color';
  .base-button {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    gap: 10px;
    padding: 0 58px;
    height: 58px;
    font-weight: 600;
    border-radius: 6px;
    background: #198fc4;
    color: #fff;
    border: none;
    cursor: pointer;
    transition:
      background 0.3s ease,
      transform 0.2s ease,
      color 0.3s ease;

    &:hover {
      background: color.adjust(#198fc4, $lightness: -8%);
      transform: translateY(-2px);
    }

    &.is-link {
      background: none;
      border: none;
      color: #198fc4;
      padding: 0;
      height: auto;

      &:hover {
        background: none;
        transform: none;
        color: color.adjust(#198fc4, $lightness: -15%);

        .icon svg path {
          fill: color.adjust(#198fc4, $lightness: -15%);
        }

        .icon {
          transform: translateX(4px);
        }
      }
    }

    &.is-arrow {
      border-radius: 28px;
      background: none;
      color: #198fc4;
      border: 2px solid #198fc4;
      padding: 0 32px;
      height: 56px;

      &:hover {
        background: #198fc4;
        color: #fff;

        .icon svg path {
          fill: #fff;
        }

        .icon {
          transform: translateX(4px);
        }
      }

      &.is-link {
        border: none;
        padding: 0;
        height: auto;
        border-radius: 0;

        &:hover {
          background: none;
          transform: none;
          color: color.adjust(#198fc4, $lightness: -15%);

          .icon svg path {
            fill: color.adjust(#198fc4, $lightness: -15%);
          }

          .icon {
            transform: translateX(4px);
          }
        }
      }

      .icon {
        display: inline-flex;
        transition:
          transform 0.3s ease,
          fill 0.3s ease;
      }
    }
  }
</style>
