<template lang="">
  <div class="headerPage">
    {{urlItem.name}}
  </div>
</template>
<script>
export default {
  data() {
    return {

    }
  },
  props: {
    urlItem: {
      default: Object,
    }
  }
}
</script>
<style lang="scss">
.headerPage {
  height: 40px !important;
  display: flex;
  justify-content: center;
  align-items: center;
  color: #183A1D;
  padding-left: 1em;
  padding-right: 1em;
  background-color: #FEFBE9 !important;
  width: 60px;

  &:hover {
    border-bottom: 2px solid #F0A04B;
    font-weight: bold;
  }
}
</style>