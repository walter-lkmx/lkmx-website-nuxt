<template>
  <div class="HeroSingleLineCode__content">
    <p class="HeroSingleLineCode__content--word-services">services</p>
    <div class="HeroSingleLineCode__content--spacer"></div>
    <p class="HeroSingleLineCode__content--page-name">.filter((service) => service.name === ‘{{page}}’);</p>
  </div>
</template>

<script>
export default {
  props: {
    page: {
        type: String,
      required: true,
    },
  }
}
</script>

<style lang="scss">
@import "@lkmx/flare/src/functions/_respond-to.scss";
.HeroSingleLineCode {
  &__content {
    display: grid;
    grid-template-columns: 19px 1fr;
    width: max-content;
    height: 40px;
    @include respond-to("<=m") {
      width: 100%;
    }
    p {
      margin-bottom: 0;
      line-height: 20px;
      font-family: var(--f-mono-text-font);
      color: var(--color-accent-cyan);
    }
    &--word-services {
      grid-column: 1 / 3;
    }
  }
} 
</style>