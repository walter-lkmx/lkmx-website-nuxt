<template>
  <nuxt-link class="nav-button__content" :to="url" :class="direction">
    <img :src="arrow" alt="" class="nav-button__arrow">
    <slot name="label"></slot>
    <img :src="cube" alt="" class="nav-button__cube">
  </nuxt-link>  
</template>

<script>
export default {
    props: {
      url: {
        type: String,
        required: false,
      },
      arrow: {
        type: String,
        required: false,
      },
      cube: {
        type: String,
        required: false,
      },
      direction: {
        type: String,
        required: true,
      },
    },
}
</script>

<style lang="scss">
  .nav-button {
    &__content {
      display: grid;
      grid-template-columns: auto 221px auto;
      gap: var(--f-gutter);
      grid-auto-flow: column;
      max-width: 499px;
      align-items: center;
      height: 142px;
      text-decoration: none;
      p {
        margin-bottom: 0;    
        line-height: 20px;    
        font-family: var(--f-mono-text-font);
      }
      &.left {
        justify-content: start;
      }
      &.right {
        justify-content: end;
        img:nth-child(1) {
          grid-column: 3;
        }
        p {
          grid-column: 2;
        }
        img:nth-child(2) {
          grid-column: 1;
        }
      }
    }
  }
</style>