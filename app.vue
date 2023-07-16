<template>
  <div class="divContainer">
    <!-- <NuxtWelcome /> -->
    <HeaderComponent />
    <NuxtPage />
    <FooterComponent />
  </div>
</template>
<style lang="scss">
@import url('~/assets/main.scss');


.divContainer {
  position: relative;
  min-height: 100vh;
}
</style>