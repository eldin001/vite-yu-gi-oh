<template>
  <div>
    <h1>{{ store.prova }}</h1>
    <HeaderComponent />
    <MainComponent />
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import MainComponent from './components/MainComponent.vue';
import {store} from './store.js'
  export default {
    name: 'App',
    data() {
      return {
        store
      }
    },
    components: {
      HeaderComponent,
      MainComponent,
    }

  }
</script>


<style lang="scss" scoped>

</style>