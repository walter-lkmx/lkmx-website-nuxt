<template>
  <simple-layout>
    <template #header>
      <simple-header mode="normal">
        <img class="header__logo" src="~/assets/img/flare--white.png">
        <nav>
          <NuxtLink to="/">Index</NuxtLink>
          <NuxtLink to="/galactic-flare">Galactic Flare</NuxtLink>
        </nav>
      </simple-header>
    </template>
    <Nuxt />
    <template #footer>
      <simple-footer>
        <p>Flare Project</p>
      </simple-footer>
    </template>
  </simple-layout>
</template>

<script>
  export default {

  }

</script>

<style lang="scss">
.header {
  &__logo {
    height: 60px;
    padding: var(--f-gutter-s) var(--f-gutter);
  }
}
</style>
