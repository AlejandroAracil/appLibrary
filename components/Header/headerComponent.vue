import { HeaderChild } from '../../.nuxt/components';
<template lang="">
  <div class="HeaderContainer">
    <NuxtLink v-for="(item, index) in filterUrlList" :key="index" :to="item.url" :style=" {'text-decoration': 'none'}">
      <HeaderChild v-if="item" :url-item="item" />
    </NuxtLink>
  </div>
</template>
<script>

export default {
  data() {
    return {
      urlList: [
        {
          name: 'Inicio',
          status: true,
          url: '/'
        },
        {
          name: 'Libros',
          status: true,
          url: '/books'
        },
        {
          name: 'Videojuegos',
          status: false,
          url: '/'
        },
        {
          name: 'Revistas',
          status: false,
          url: '/'
        },
      ]
    }
  },
  computed: {

    filterUrlList() {
      return this.urlList //.filter(x => x.status) || [];
    }

  },
  mounted() {
  },
}
</script>
<style scoped lang="scss">
// @import url('~/assets/main.css');

.HeaderContainer {
  background-color: #FEFBE9 !important;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: flex-start;
  align-items: center;
  align-content: center;

  padding-top: 0.5em;
  padding-bottom: 0.5em;
  padding-left: 5em;
  padding-right: 5em;

  height: 50px !important;


  // border-radius: 12px;
  border: 1px solid #F0A04B;

  gap: 5em;

  // margin-left: 1em;
  // margin-right: 1em;
  margin-bottom: 1em;

}
</style>