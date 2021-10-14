<template>
  <section class="hero-app-maintenance__content">
    <div class="hero-app-maintenance__description-content">
      <hero-single-line-code page="application-maintenance-support"/>
      <slot name="title"></slot>
      <div class="hero-app-maintenance__description-content--paragraph">
        <slot name="paragraph"></slot>
      </div>
    </div>
    <div class="hero-app-maintenance__content--image">
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
  &__hero-app-maintenance {
    .hero-app-maintenance__content {
      display: grid;
      grid-template-columns: 686px 1fr;
      height: max-content;
      margin-top: 50px;

      .hero-app-maintenance__description-content {
        display: grid;
        gap: 12px;
        padding: var(--f-gutter);
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
            width: 92%;
            margin-bottom: 0;
          }
        }
      }
      &--image {
        position: relative;
        img {
          max-width: unset;
          height: 751px;
          position: absolute;
          transform: translate(-96px, -73px);
          z-index: 20;
        }
      }
    }
  }
  
}
</style>