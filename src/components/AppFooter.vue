<template>
    <footer>
        <h4>

        </h4>
        <ul>
            <li v-for="restaurant, i in restaurantsInfo" :key="i">
                {{ restaurant.street }}
                {{ restaurant.city }}
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

}
</style>>
