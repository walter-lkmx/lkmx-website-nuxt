<template>
  <section class="rubbon-services">
    <div class="rubbon-services__content">
      <slot></slot>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss">
@import "@lkmx/flare/src/functions/_respond-to.scss";

/* #body-index {
  &__rubbon-services {
    background: var(--color-accent-blue-01); 
    .content {
      .box {
        padding: 0;
      }
    }   
  }
}
.rubbon-services {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  &__content {
    grid-column: 2;
    p {
      color: var(--color-neutral-white);
      line-height: 20px;
      margin: 0;
      width: 90%;
    }
  }
} */
</style>