<template>
    <footer>
        <h4>
            find our restaurant
        </h4>
        <ul>
            <li v-for="restaurant, i in restaurantsInfo" :key="i">
                {{ restaurant.street }}
                <br>
                {{ restaurant.city }}
                <br>
                {{ restaurant.phone }}
            </li>
        </ul>
    </footer>
</template>

<script>
export default {
    name: 'AppFooter',
    props: {
        restaurantsInfo: Array
    }
}
</script>

<style lang="scss" scoped>
footer {
    background-color: #181818;
    padding: 30px;

    h4 {
        color: #b7903c;
        text-transform: uppercase;
    }

    li {
        margin: 20px 0;
        color: #858585;
    }
}
</style>>
