<template>
    <div class="product_card">
        <img :src="require(`../assets/img/products/${product.pic}`)" :alt="product.name">
        <div class="sold_out">
            sold
        </div>
        <h4>
            {{ product.name }} 
        </h4>
        <h4>
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

</style>
