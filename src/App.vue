<template>
  <div>
    <HeaderComponent />
    <MainComponent />
  </div>
</template>

<script>
import {store} from './store.js';
import axios from 'axios';
import HeaderComponent from './components/HeaderComponent.vue';
import MainComponent from './components/MainComponent.vue';
  export default {
    name: 'App',
    components: {
      HeaderComponent,
      MainComponent,
    },
    data() {
      return {
        store,
      }
    },
    methods: {
      getCards(){
        axios.get(this.store.apiUrl + thisStore.endPoint.cards, this.store.options).then((res) =>{
          this.store.cards = res.data.data.map((card) => {
            return{
              id: card.id,
              title: card.name,
              image: card.card_image[0].image.url,
              status: card.archetype,
            }
          });
          this.store.total = res.data.meta.total_rows;
        }).catch((error) => {
          this.store.error.message = error.message;
        })

      },
      created() {
        this.getCards();
      },
    }


  }
</script>


<style lang="scss" scoped>

</style>