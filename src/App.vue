<script>
import appHeader from './components/appHeader.vue';
import appMain from './components/appMain.vue';
import appCard from './components/appCard.vue';
import appFooter from './components/appFooter.vue';

export default {
    components: {
        appHeader,
        appMain,
        appCard,
        appFooter
    }
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