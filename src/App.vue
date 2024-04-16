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
import {store} from './store.js';
import axios from 'axios';
  export default {
    name: 'App',
    components: {
      HeaderComponent,
      MainComponent,
    },
    data() {
      return {
        store
      }
    },
    methods: {
      getCards(){
        this.store.loadign = true;
        this.store.error.message = null;
        axios.get(this.store.apiUrl + thisStore.endPoint.cards, this.store.options).then((res) =>{
          this.store.cards = res.data.data;
          this.store.total = res.data.meta.total_rows;
        }).catch((error) => {
          this.store.error.message = error.message;
        })

      }
    }


  }
</script>


<style lang="scss" scoped>

</style>