<template>
    <div class="container d-flex flex-wrap">
        <div class="col-12 col-md-6 col-lg-3" v-for="card in store.cards" :key="card.id">
            <CardComponent :id="card.id" :title="card.title" :image="card.image" :status="card.status" />
        </div>
    </div>
</template>

<script>
import { store } from '../store.js';
import CardComponent from './CardComponent.vue';
export default {
    name: 'CardListComponent',
    components: {
        CardComponent,
    },
    data() {
        return {
            store,
        }
    },  
}
</script>

<style lang="scss" scoped></style>