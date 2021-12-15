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
    </main>
</template>

<script>
import TeamCard from "@/components/TeamCard.vue";


export default {
    name: 'AppMain',
    components: {
        TeamCard
    },
    props: {
        thumbs: Array,
        menus: Array
    },
    data() {
        return {
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
}
</style>