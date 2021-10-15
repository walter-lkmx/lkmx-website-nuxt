<template>
  <div class="nav-button" :class="direction">
    <nuxt-link class="nav-button__content" :to="url">
    <img :src="arrow" alt="" class="nav-button__arrow">
    <slot name="label"></slot>
    <img :src="cube" alt="" class="nav-button__cube">
    </nuxt-link>
  </div>  
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
@import "@lkmx/flare/src/functions/_respond-to.scss";
  .nav-button {
    @include respond-to(">=xl") {
      max-width: 499px;
    }
    &__content {
      display: grid;
      grid-template-columns: auto 221px auto;
      gap: var(--f-gutter);
      grid-auto-flow: column;
      width: fit-content;
      align-items: center;
      height: 142px;
      text-decoration: none;
      @include respond-to("<=s") {
        margin: auto;
      }
      p {
        margin-bottom: 0;    
        line-height: 20px;    
        font-family: var(--f-mono-text-font);
      }
    }
    &.left {
      justify-content: start;
    }
    &.right {
      justify-self: end;
      @include respond-to("<=s") {
        justify-content: center;
        width: 100%;
      }
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
</style>