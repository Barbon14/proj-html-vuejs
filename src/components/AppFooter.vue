<template>
    <footer>
        <section id="footer_info">
            <div>
                <h4 class="text_gold">
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
                <h4 class="text_gold">
                    working hours
                </h4>
                <ul>
                    <li v-for="timeInfo, i in workingTime" :key="i">
                        <h6 class="text_gold" >
                            {{ timeInfo.day }}
                        </h6>
                        <div :class="timeInfo.hours.toLowerCase().includes('closed') ? 'text_red' : null">
                            {{ timeInfo.hours }}
                        </div>
                    </li>
                </ul>

                <div class="socials">
                    <h6 class="text_gold">
                        follow us:
                    </h6>
                    <ul>
                        <li 
                            v-for="social, i in socials" 
                            :key="`social-${i}`"
                        >
                            <a :href="social.href">
                                <i :class="social.icon"></i>
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
            <h2>
                the don peppe crew first and foremost values an authentic, well baked slice of pizza.
            </h2>
        </section>
        <img src="../assets/img/footer-img-1.jpg" alt="">
    </footer>
</template>

<script>
export default {
    name: 'AppFooter',
    props: {
        restaurantsInfo: Array,
        workingTime: Array,
        socials: Array
    }
}
</script>

<style lang="scss" scoped>
footer {
    background-color: #181818;
    display: flex;
    height: 630px;

    a {
        color: white;
    }

    #footer_info {
        width: 50%;
        padding: 50px;
        padding-top: 100px;
        display: flex;
        justify-content: space-between;
    }

    h2 {
        width: 33%;
        color: white;
    }

    li {
        margin: 20px 0;
        color: #858585;
    }
    
    img {
        width: 50%;
        object-fit: cover;
    }

    .socials {
        display: flex;
        align-items: center;

        ul {
            display: flex;

            li {
                margin: 0 5px;
            }
        }
    }
}
</style>>
