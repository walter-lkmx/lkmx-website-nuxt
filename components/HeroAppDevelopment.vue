<template>
  <section class="hero-app-development__content">
    <div class="hero-app-development__description-content">
      <slot name="description"></slot>
    </div>
    <div class="hero-app-development__image-content">
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
  &__hero-app-development {
    .hero-app-development__content {
      display: grid;
      grid-template-columns: auto 1fr;
      height: max-content;
      align-self: center;

      .hero-app-development__description-content {
        display: grid;
        gap: 12px;
        padding: var(--f-gutter);
        /* margin-top: 92px; */

        p, h1 {
          margin-bottom: 0;
        }
        p:first-child {
          color: var(--color-accent-cyan);
          font-family: var(--f-mono-text-font);
          line-height: 20px;
        }
        h1 {
          color: var(--color-accent-pink);
          letter-spacing: -1px;
          font-weight: var(--f-h2-text-weight);
        }
        p:last-child {
          color: var(--color-neutral-white);
          font-size: var(--f-h3-text-size);
          line-height: var(--f-h3-line-height);
          width: 108%;
        }
      }
      .hero-app-development__image-content {
        position: relative;
        img {
          max-width: unset;
          height: 751px;
          /* top: -52px;
          right: -190px; */
          position: absolute;
          transform: translate(-67px, -78px);
          z-index: 20;
        }
      }
    }
  }
  
}
</style>