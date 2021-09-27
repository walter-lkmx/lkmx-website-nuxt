<template>
  <section class="my-services">
    <div class="my-services__title-content">
      <slot name="title"></slot>
    </div>
    <div class="my-services__content">
      <div class="my-services_side-a">
        <slot name="side-a"></slot>
      </div>
      <div class="my-services_side-b">
        <slot name="side-b"></slot>
      </div>
      <div class="my-services_side-c">
        <slot name="side-c"></slot>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss">
@import "@lkmx/flare/src/functions/_respond-to.scss";

#body-index {
  &__my-services {
    
  }
}
.my-services {
  &__title-content {
    border: 1px solid red;
    text-align: center;
    padding-top: 110px;
    p {
      color: var(--color-neutral-gray-01);
    }
    p strong {
      font-weight: bold;
    }
  }
  &__content {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    border: 1px solid blue;
    img {
      width: 204px;
      height: auto;
    }
    h4 {
      color: var(--color-accent-pink);
    }
    p {
      color: var(--color-neutral-gray-01);
    }
  }
}
</style>