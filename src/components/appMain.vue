<template>



    <main class="page-content">
        <section>
            <div class="container">
                <div class="row">
                    <div v-for="product in store.products" :key="product.id" class="col-4 col-6 col-12 ">
                        <appCard :product="product" />
                    </div>



                </div>
            </div>
        </section>

    </main>

</template>

<script>
import appCard from '../assets/appCard.vue';
// import data from '../assets/db.json'
import { store } from '../store.js';
export default {
    components: {
        appCard

    },
    data() {
        return {
            store: store,

        }
    }
}
</script>

<style lang="scss"></style>