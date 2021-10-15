<template>
  <section class="hero-discovery__content">
    <div class="hero-discovery__description-content">
      <hero-single-line-code page="discovery"/>
      <slot name="title"></slot>
      <div class="hero-discovery__description-content--paragraph">
        <slot name="paragraph"></slot>
      </div>
    </div>
    <div class="hero-discovery__content--image">
      <slot name="image"></slot>
    </div>
  </section>  
</template>

<script>
export default {

}
</script>

<style lang="scss">
@import "@lkmx/flare/src/functions/_respond-to.scss";

#body-index {
  &__hero-discovery {
    .hero-discovery__content {
      display: grid;

      justify-content: end;
      height: max-content;
      @include respond-to(">=xl") {
        grid-template-columns: 533px 507px;
      }
      @include respond-to("<=m") {
        grid-template-columns: 1fr;
      }
      .hero-discovery__description-content {
        display: grid;
        gap: 12px;
        padding: var(--f-gutter);
        margin-top: 92px;
        @include respond-to("<=l") {
          margin-top: 0;
        }
        h1 {
          color: var(--color-accent-pink);
          letter-spacing: -1px;
          font-weight: var(--f-h2-text-weight);
          margin-bottom: 0;
        }
        &--paragraph {
          p {
            color: var(--color-neutral-white);
            font-size: var(--f-h3-text-size);
            line-height: var(--f-h3-line-height);
            width: 104%;
            margin-bottom: 0;
            @include respond-to("<=l") {
              width: 100%;
            }
          }
        }
      }
    &--image {
        position: relative;
        img {
          max-width: inherit;
          height: 690px;
          transform: translate(18px, -20px);
          position: absolute;
          z-index: 20;
          @include respond-to("<=l") {
            height: 300px;
            position: unset;
            transform: unset;
          }
        }
      }
    }
  }
  
}
</style>