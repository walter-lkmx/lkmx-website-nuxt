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
      grid-template-columns: 533px 507px;
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
      .hero-discovery__image-content {
        position: relative;
        img {
          max-width: inherit;
          height: 690px;
          transform: translate(18px, -20px);
          position: absolute;
          z-index: 20;
        }
      }
    }
  }
  
}
</style>