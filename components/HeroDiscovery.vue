<template>
  <section class="hero-discovery__content">
    <div class="hero-discovery__description-content">
      <slot name="description"></slot>
    </div>
    <div class="hero-discovery__image-content">
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
      grid-template-columns: 1fr 1fr;
      justify-content: end;

      .hero-discovery__description-content {
        display: grid;
        gap: 12px;
        padding: var(--f-gutter);
        margin-top: 92px;

        p, h1 {
          margin-bottom: 0;
        }
        p:first-child {
          color: var(--color-accent-cyan);
          height: 40px;
        }
        h1 {
          color: var(--color-accent-pink);
          letter-spacing: -1px;
          font-weight: var(--f-h2-text-weight);
        }
        p:last-child {
          color: var(--color-neutral-white);
          width: 110%;
          font-size: var(--f-h3-text-size);
          line-height: var(--f-h3-line-height);
        }
      }
      .hero-discovery__image-content {
        position: relative;
        img {
          max-width: inherit;
          height: 690px;
          transform: translate(31px, -20px);
          position: absolute;
          z-index: 20;
        }
      }
    }
  }
  
}
</style>