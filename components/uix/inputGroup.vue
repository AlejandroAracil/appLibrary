<template >
  <div class="divFormGroup">
    <span class="tagFormGroup"> {{ tag }}</span>
    <input class="inputFormGroup" type="text" :value="value">
  </div>
</template>
<script>
export default {
  data() {
    return {

    }
  },
  props: {
    tag: {
      type: String,
      default: '',
    },
    value: {
      default: ''
    }
  }
}
</script>
<style lang="scss">
.divFormGroup {
  display: flex;
  align-content: stretch;
  // border-radius: 5px;
  padding: 5px;
  color: #183A1D;
}

.tagFormGroup {
  background-color: #FEFBE9;
  padding: 7px;
  border-top: 2px solid #F0A04B;
  border-bottom: 2px solid #F0A04B;
  border-left: 2px solid #F0A04B;
  border-right: 1px solid #F0A04B;

  border-radius: 3px 0px 0px 3px;
}

.inputFormGroup {
  border-top: 2px solid #F0A04B;
  border-bottom: 2px solid #F0A04B;
  border-right: 2px solid #F0A04B;
  border-left: 0px;

  border-radius: 0px 8px 8px 0px;
}
</style>