<template>
    <div class="product_card">
        <img :src="require(`../assets/img/products/${product.pic}`)" :alt="product.name">
        <div class="sold_out" v-if="product.sold">
            sold
        </div>
        <h4 class="text_gold">
            {{ product.name }} 
        </h4>
        <h4 class="text_orange">
            {{ product.price }}
        </h4>
    </div>
</template>

<script>
export default {
    name: 'ProductCard',
    props: {
        product: Object
    }
}
</script>

<style lang="scss" scoped>
.product_card {
    position: relative;
    text-align: center;

    img {
        width: 180px;
        margin-bottom: 15px;
    }

    .sold_out {
        background-color: #d2401e;
        border-radius: 50%;
        color: white;
        text-transform: uppercase;
        font-size: 10px;
        width: 40px;
        height: 40px;
        // flex
        display: flex;
        justify-content: center;
        align-items: center;
        // position
        position: absolute;
        top: 30px;
        right: -15px;
        transform: translate(-50%, -50%);
    }
}
</style>
