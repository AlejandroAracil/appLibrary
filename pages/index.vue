import { UixInputGroup } from '../.nuxt/components';
<template lang="">
  <div>
    <h1 class="titlePage"><strong> Página Inicio - Tareas y metas del <u>Proyecto</u> </strong></h1>
    <hr>
    <Icon name="uil:github" color="black" />
    <button @click="addTask()">ADD</button>

    <UixInputGroup tag="Título Lista" />

    <h6 v-for="(item, index) in lists" :key="index"> {{ item }}</h6>

  </div>
</template>
<script>
export default {
  data() {
    return {
      lists: []
    }
  },
  mounted() {
    this.checkLocalStorage()
  },
  methods: {
    checkLocalStorage() {
      if (!localStorage.getItem('lists')) {
        localStorage.setItem('lists', '[]')
      }
      this.lists = JSON.parse(localStorage.getItem('lists'));
    },
    addTask() {
      this.lists.push(1231231321231)
    }
  },
  computed: {
    getListsLocalStorage() {
      return JSON.parse(localStorage.getItem('lists') || '[]')
    }
  },
  watch: {
    lists: {
      handler(newVal, oldVal) {
        localStorage.setItem('lists', JSON.stringify(this.lists))
      },
      deep: true
    }
  }
}
</script>
<style lang="scss">
.titlePage {
  text-align: center;
}
</style>