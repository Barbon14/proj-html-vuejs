<template>
    <main>
        <section>
            <img 
                class="thumb"
                v-for="thumb, i in thumbs" 
                :key="`thumb-${i}`"
                :src="require(`../assets/img/jumbo/${thumb}`)" 
                alt=""
            >
        </section>
        <section id="testimonials">
            <i class="fas fa-quote-left"></i>
            <h3>
                "forget the trendy pizza shops, this hidden spot makes the best new york-style pizza slice in naples"
            </h3>
            <h6>
                washington post 2018
            </h6>
        </section>
        <section id="menu_list">
            <div class="section_img">
                <img src="../assets/img/h1-img-4.jpg" alt="">
                <img src="../assets/img/h1-img-7n.png" alt="">
            </div>
            <div id="menu_info">
                <div>
                    <h2>
                        specials*
                    </h2>
                    <span class="text_gray">
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Nesciunt, numquam
                    </span>
                    <div
                        class="menu" 
                        v-for="menu, i in menus" 
                        :key="`menu-${i}`"
                    >
                        <h3 class="price text_red">
                            {{ menu.price }}
                        </h3>
                        <div>
                            <h3>
                                {{ menu.name }}
                            </h3>
                            <div class="description text_gray">
                                {{ menu.description }}
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <section id="disclaimer">
            <h2>
                go ahead and build your own pizza we wont't judge!
            </h2>
        </section>
        <section id="team">
            <TeamCard
                v-for="mate, i in teamInfo"
                :key="`mate-${i}`"
                :mate="mate"
            />
        </section>
        <section id="clients">
            <div
                v-for="client, i in clients"
                :key="`client-${i}`"
            >
                <a :href="client.href">
                    <img 
                        :src="require(`../assets/img/clients/${client.logo}`)" 
                        :alt="client.name"
                    >
                </a>
            </div>
        </section>
        <section id="products">
            <div class="products_info">
                <h6 class="text_orange">
                    chose your flavor
                </h6>
                <h2>
                    the best pizza menu in town
                </h2>
                <p class="text_gray">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Natus ea doloremque aut nam optio error inventore, consectetur harum repellat provident.
                </p>
            </div>
            <div class="products_list">
                <ProductCard
                    v-for="product, i in productsInfo"
                    :key="`product-${i}`"
                    :product="product"
                />
            </div>
        </section>
        <section id="events">
            <div class="event_list">
                <h6 class="text_brown">
                    made with love
                </h6>
                <h2>
                    delish pizza deals
                </h2>
                <EventCard
                    v-for="event, i in eventsInfo"
                    :key="`event-${i}`"
                    :event="event"
                />
            </div>
            <div class="section_img">
                <img src="../assets/img/h3-img-5a.jpg" alt="">
            </div>
        </section>
        <section id="reservation">
            <form action="#">
                <span class="form_input">
                    <input type="text" placeholder="1 Person">
                    <i class="fas fa-user-friends"></i>
                </span>
                <span>
                    for
                </span>
                <span class="form_input">
                    <input type="text" placeholder="11/29/2020">
                    <i class="far fa-calendar"></i>
                </span>
                <span>
                    at
                </span>
                <span class="form_input">
                    <input type="text" placeholder="7:00 pm">
                    <i class="far fa-clock"></i>
                </span>
                <a href="#" class="btn">
                    book a table 
                </a>
            </form>
        </section>
    </main>
</template>

<script>
import TeamCard from "@/components/TeamCard.vue";
import ProductCard from "@/components/ProductCard.vue";
import EventCard from "@/components/EventCard.vue";

export default {
    name: 'AppMain',
    components: {
        TeamCard,
        ProductCard,
        EventCard
    },
    props: {
        thumbs: Array,
        menus: Array,
        clients: Array
    },
    data() {
        return {

            //team components
            teamInfo: [
                {
                    pic: 'h1-team-1a-700x700.jpg',
                    name: 'peter anderson',
                    role: 'Head Chef',
                    instagram: '#',
                    twitter: '#',
                    facebook: '#'
                },
                {
                    pic: 'h1-team-2a.jpg',
                    name: 'sharon hayes',
                    role: 'Executive Chef',
                    instagram: '#',
                    twitter: '#',
                    facebook: '#'
                },
                {
                    pic: 'h1-team-4a.jpg',
                    name: 'frank bailey',
                    role: 'Kitchen porter',
                    instagram: '#',
                    twitter: '#',
                    facebook: '#'
                },
                {
                    pic: 'h1-team-3a.jpg',
                    name: 'carol simpson',
                    role: 'Sous Chef',
                    instagram: '#',
                    twitter: '#',
                    facebook: '#'
                }
            ],

            //products info
            productsInfo: [
                {
                    pic: 'h3-product-img-1a-100x100.png',
                    name: 'bismarck',
                    price: '$30.00',
                    sold: false
                },
                {
                    pic: 'h3-product-img-2a-150x150.png',
                    name: 'fiori di zucca',
                    price: '$7.00 - $50.00',
                    sold: false
                },
                {
                    pic: 'h3-product-img-3a-150x150.png',
                    name: 'valdostana',
                    price: '$55.00',
                    sold: true
                },
                {
                    pic: 'h3-product-img-4a-150x150.png',
                    name: 'pizza tartufata',
                    price: '$45.00',
                    sold: false
                },
                {
                    pic: 'h3-product-img-5a-150x150.png',
                    name: 'francescana',
                    price: '$25.00',
                    sold: false
                },
                {
                    pic: 'h3-product-img-6a-100x100.png',
                    name: 'campagnola',
                    price: '$50.00 - $95.00',
                    sold: false
                }
            ],

            eventsInfo: [
                {
                    day: '02',
                    month: 'nov',
                    name: 'traditional neapolitan pies in kyoto pizza mercato',
                    address: '204 e. pizzetta tommaso'
                },
                {
                    day: '03',
                    month: 'nov',
                    name: 'terarazza patio dining space opening this weekend',
                    address: '204 e. pizzetta tommaso'
                },
                {
                    day: '05',
                    month: 'nov',
                    name: 'sienna private dining room with stépahane brunn',
                    address: '204 e. pizzetta tommaso'
                }
            ]
        }
    }
}
</script>
    
<style lang="scss" scoped>
main {

    .thumb {
        width: calc(25% - 10px);
        margin: 0 5px;
    }

    .section_img {
        width: 50%;
        position: relative;

        img {
            width: 100%;
        }
    }

    #testimonials {
        background-image: url('../assets/img/h3-testimonials-bckgrnd.jpg');
        background-position: center;
        height: 450px;
        text-transform: uppercase;
        text-align: center;
        // flex
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;

        .fas {
            color: #b7903c;
            font-size: 50px;
            margin-bottom: 20px;
        }

        h3 {
            width: 36%;
            margin-bottom: 10px;
            font-weight: 500;
        }

        h6 {
            color: #ca3e12;
            font-weight: 500;
        }
    }

    #menu_list {
        display: flex;

        .section_img {
            
            img:last-of-type {
                position: absolute;
                top: 50%;
                left: 50%;
                transform: translate(-50%, -50%);
                width: 40%;
            }
        }

        #menu_info {
            width: 50%;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;

            h2,
            h3 {
                margin-bottom: 5px;
                font-weight: 500;
            }

            h2 {
                font-size: 30px;
            }

            &> div {
                width: 450px;
            }

            .menu {
                margin: 20px 0px;
                display: flex;

                .price {
                    width: 45px;
                }

                .description {
                    font-size: 14px;
                }
            }
        }
    }

    #disclaimer {
        background-image: url('../assets/img/h3-background-img.jpg');
        padding: 120px 66% 120px 15%;

        h2 {
            font-size: 55px;
            color: white;
        }
    }

    #team {
        display: flex;
        background-image: radial-gradient(#d1d4d8 1px,transparent 1px),radial-gradient(#d1d4d8 1px,transparent 1px);
    }

    #clients{
        background-color: #f7f7f2;
        padding: 80px 0;
        display: flex;
        justify-content: center;

        img {
            height: 125px;
        }
    }

    #products {

        .products_info {
            padding: 0 30%;
            text-align: center;
        }

        .products_list {
            display: flex;
            justify-content: space-around;
            padding: 80px 0;
        }
    }

    #events {
        background-color: #181818;
        display: flex;
        padding: 0;
        color: white;

        .event_list {
            width: 50%;
            padding: 180px;
            padding-right: 280px;
        }

        .event_card:last-of-type {
            border: none;
        }
    }

    #reservation {
        text-transform: uppercase;
        padding: 80px 250px;
        background-image: url(../assets/img/h3-background-img-3.jpg);
        background-size: cover;
        background-repeat: no-repeat;
        color: white;
        
        form {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        a {
            color: white;
        }

        .form_input {
            position: relative;

            input {
                padding: 18px;
                border: 1px solid black;  
            }
            
            .fas,
            .far {
                position: absolute;
                top: 18px;
                right: 20px;
                color: #b7903c;
            }
        }
    }
}
</style>