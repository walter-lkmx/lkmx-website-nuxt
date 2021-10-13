<template>
  <section class="HelpSectionAppDevelopment__content">
      <div class="HelpSectionAppDevelopment__content-side-a">
        <slot name="title-side-a"></slot>
        <slot name="description-side-a"></slot>
      </div>
      <div class="HelpSectionAppDevelopment__content-side-b">
        <slot name="title-side-b"></slot>
        <slot name="description-side-b"></slot>
      </div>
  </section>
</template>

<script>
export default {

}
</script>

<style lang="scss">
@import "@lkmx/flare/src/functions/_respond-to.scss";
.HelpSectionAppDevelopment__content {
  display: grid;
  gap: var(--f-gutter-xl);
  .HelpSectionAppDevelopment__content-side-a, .HelpSectionAppDevelopment__content-side-b {
    display: grid;
    grid-template-rows: 20px 1fr;
    gap: var(--f-gutter);   
    p {
      margin-bottom: 0;
    }
    p:first-child {
      font-family: var(--f-mono-text-font);
      color: var(--color-accent-pink);
      font-weight: var(--f-default-headers-weight);
      margin-bottom: 0;
      line-height: 20px;
    }
    p:last-child {
      color: var(--color-neutral-gray-01);
      height: 96px;
    }
  }
}
</style>