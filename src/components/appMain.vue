<template>



    <main class="page-content">
        <section>
            <div class="container">
                <div class="row">
                    <div v-for="product in products " :key="product.id" class="col-4 col-6 col-12 ">
                        <div class="card-product">
                            <div class="card-header">
                                <img :src="'/' + product.frontImage" alt="">
                                <img class="overlay" :src="'/' + product.backImage" alt="">
                                <ul class="badge-container">
                                    <li v-for="(badge, i) in product.badges" :key="i" :class="`badge--${badge.type}`"
                                        class=" badge ">
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
                    </div>



                </div>
            </div>
        </section>

    </main>

</template>

<script>
export default {
    data() {
        return {
            "products": [
                {
                    "id": 1,
                    "frontImage": "1.webp",
                    "backImage": "1b.webp",
                    "brand": "Levi's",
                    "name": "Relaxed Fit",
                    "price": 29.99,
                    "isInFavorites": true,
                    "badges": [
                        {
                            "type": "tag",
                            "value": "Sostenibilità"
                        },
                        {
                            "type": "discount",
                            "value": "-50%"
                        }
                    ]
                },
                {
                    "id": 2,
                    "frontImage": "2.webp",
                    "backImage": "2b.webp",
                    "brand": "Guess",
                    "name": "Roses Tee",
                    "price": 20.99,
                    "isInFavorites": true,
                    "badges": [
                        {
                            "type": "discount",
                            "value": "-30%"
                        }
                    ]
                },
                {
                    "id": 3,
                    "frontImage": "3.webp",
                    "backImage": "3b.webp",
                    "brand": "Come Zucchero Filato",
                    "name": "Voglia di colori pastello",
                    "price": 129.99,
                    "isInFavorites": false,
                    "badges": [
                        {
                            "type": "discount",
                            "value": "-30%"
                        }
                    ]
                },
                {
                    "id": 4,
                    "frontImage": "4.webp",
                    "backImage": "4b.webp",
                    "brand": "Levi's",
                    "name": "Tee Unisex",
                    "price": 14.99,
                    "isInFavorites": false,
                    "badges": [
                        {
                            "type": "tag",
                            "value": "Sostenibilità"
                        },
                        {
                            "type": "discount",
                            "value": "-50%"
                        }
                    ]
                },
                {
                    "id": 5,
                    "frontImage": "5.webp",
                    "backImage": "5b.webp",
                    "brand": "Maya Deluxe",
                    "name": "Stripe Bodice",
                    "price": 99.99,
                    "isInFavorites": true,
                    "badges": [
                        {
                            "type": "tag",
                            "value": "Sostenibilità"
                        },
                        {
                            "type": "discount",
                            "value": "-50%"
                        }
                    ]
                },
                {
                    "id": 6,
                    "frontImage": "6.webp",
                    "backImage": "6b.webp",
                    "brand": "Esprit",
                    "name": "Maglione - Black",
                    "price": 29.99,
                    "isInFavorites": true,
                    "badges": [
                        {
                            "type": "tag",
                            "value": "Sostenibilità"
                        }
                    ]
                }
            ]
        }
    }
}
</script>

<style lang="scss">
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