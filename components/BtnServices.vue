<template>
  <nuxt-link class="btn-services" :to="url">
    <h4><slot name="btn-services-title"></slot></h4>
    <p><slot name="btn-services-description"></slot></p>
    <slot name="btn-services-image"></slot>
  </nuxt-link>
</template>

<script>
export default {
  props: {
      url: {
        type: String,
        required: true,
      },
  },
}
</script>

<style lang="scss">
  @import "@lkmx/flare/src/functions/_respond-to.scss";
  #body-index {
    &__services-cubes {
      .btn-services {
        display: grid;
        gap: var(--f-gutter);
        text-decoration: none;
        &:hover {
          h4 {
            color: var(--color-accent-blue-01);
          }
          p:nth-child(3) {
            border-block-end: 1px solid var(--color-accent-blue-01);
          }
        }
        p {
          margin-bottom: 0;
          color: var(--color-neutral-gray-01);
        }
        img {
          height: 32px;
        }
        h4 {
          color: var(--color-accent-pink);
          margin: 0;
          position: relative;
          letter-spacing: 0.5px;
          height: 52px;
          font-weight: var(--f-h2-text-weight);
        }
        p:nth-child(3) {
          width: max-content;
        }
      }
    }
  }
</style>