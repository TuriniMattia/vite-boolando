<template>
    <div class="card-product">
        <div class="card-header">
            <img :src="'/' + product.frontImage" alt="">
            <img class="overlay" :src="'/' + product.backImage" alt="">
            <ul class="badge-container">
                <li v-for="(badge, i) in product.badges" :key="i" :class="`badge--${badge.type}`" class=" badge ">
                    {{ badge.value }}
                </li>
                <!-- <li class="badge badge--tag">sostenibilita</li> -->
            </ul>
            <a href="" class="hearts-badge">
                <p>&hearts;</p>
            </a>
        </div>
        <div class="card-body">
            <p>{{ product.brand }}</p>
            <h3>{{ product.name }}</h3>
            <p>{{ product.price }}</p>

        </div>
    </div>
</template>

<script>
export default {
    props: ['product'],
    data() {


        return {}
    }
}
</script>

<style lang="scss" scoped>
.badge {
    line-height: 30px;
    font-size: 14px;
    padding: 0 12px;
    color: white;
    font-weight: 300;
}

.badge--tag {
    background-color: #008000;
    display: inline-block;


}

.badge--discount {
    background-color: #FF0000;
    display: inline-block;

}


.badge-container {
    position: absolute;
    bottom: 20px;
}



.card-header {
    position: relative;

}

.card-header>img {
    display: block;
}

.overlay {
    position: absolute;
    width: 100%;
    height: 100%;
    opacity: 0;
    top: 0;
    left: 0;
    transition: opacity 500ms;
}

.card-product:hover .overlay {
    opacity: 1;
}

.hearts-badge {
    font-size: x-large;
    background-color: white;
    display: inline-block;
    width: 40px;
    line-height: 20px;
    padding: 10px;
    position: absolute;
    top: 10px;
    right: 0;
    text-align: center;
}
</style>