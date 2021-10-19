<template>
  <section class="hero-app-development__content">
    <div class="hero-app-development__description-content">
      <hero-single-line-code page="application-development"/>
      <slot name="title"></slot>
      <div class="hero-app-development__description-content--paragraph">
        <slot name="paragraph"></slot>
      </div>
    </div>
    <div class="hero-app-development__content--image">
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
      height: max-content;
      margin-top: 54px;
      @include respond-to(">=xl") {
        grid-template-columns: 686px 1fr;
      }
      @include respond-to("<=m") {
        grid-template-columns: 1fr;
        margin-top: 0;
      }
      .hero-app-development__description-content {
        display: grid;
        gap: 12px;
        padding: var(--f-gutter);
        h1 {
          color: var(--color-accent-pink);
          letter-spacing: -1px;
          font-weight: var(--f-h2-text-weight);
          margin-bottom: 0;
          @include respond-to("<=xs") {
            font-size: 50px;
            line-height: 67px;
          }          
        }
        &--paragraph {
          p {
            color: var(--color-neutral-white);
            font-size: var(--f-h3-text-size);
            line-height: var(--f-h3-line-height);
            width: 92%;
            margin-bottom: 0;
            @include respond-to("<=l") {
              width: 100%;
              @include respond-to("<=xs") {
                font-size: var(--f-default-text-size);
                line-height: var(--f-paragraph-line-height);
              }
            }
          }
        }
      }
      &--image {
        position: relative;
        img {
          max-width: unset;
          height: 751px;
          position: absolute;
          transform: translate(-96px, -77px);
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