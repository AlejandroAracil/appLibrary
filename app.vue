<template>
  <div class="divContainer">
    <!-- <NuxtWelcome /> -->
    <HeaderComponent />
    <div class="divInfoPage">
      <NuxtPage />
    </div>
    <FooterComponent />
  </div>
</template>
<style lang="scss">
@import url('~/assets/main.scss');


.divContainer {
  position: relative;
  min-height: 100vh;
}

.divInfoPage {
  margin: 1em 1em;
}
</style>