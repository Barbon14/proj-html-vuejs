<template>
    <footer>
        <section id="footer_info">
            <div>
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
            </div>
            <div>
                <h4>
                    working hours
                </h4>
                <ul>
                    <li v-for="timeInfo, i in workingTime" :key="i">
                        <h6>
                            {{ timeInfo.day }}
                        </h6>
                        {{ timeInfo.hours }}
                    </li>
                </ul>
            </div>
        </section>
        <img :src="require('../assets/img/footer-img-1.jpg')" alt="">
    </footer>
</template>

<script>
export default {
    name: 'AppFooter',
    props: {
        restaurantsInfo: Array,
        workingTime: Array
    }
}
</script>

<style lang="scss" scoped>
footer {
    background-color: #181818;
    display: flex;

    #footer_info {
        width: 50%;
        padding: 30px;
        display: flex;
        justify-content: space-between;
    }

    h4, 
    h6 {
        color: #b7903c;
        text-transform: uppercase;
    }

    li {
        margin: 20px 0;
        color: #858585;
    }
    
    img {
        width: 50%;
    }
}
</style>>
