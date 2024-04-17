<script>
import appHeader from './components/appHeader.vue';
import appMain from './components/appMain.vue';
import appCard from './assets/appCard.vue';
import appFooter from './components/appFooter.vue';
import axios from 'axios';
import { store } from './store'

export default {
    components: {
        appHeader,
        appMain,
        appCard,
        appFooter
    },
    methods: {
        fetchProducts() {
            axios.get('http://localhost:3000/products').then(() => {
                store.products = res.data
            })
        }
    },
    created() {
        this.fetchProducts()
    },
}
</script>

<template>
    <div>
        <appHeader />
        <appMain />
        <appFooter />


    </div>
</template>



<style lang="scss">
@use './assets/scss/general';
</style>