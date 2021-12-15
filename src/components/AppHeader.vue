<template>
    <header id="top">
        <nav>
            <!-- order online -->
            <a href="#" class="btn">
                order online
            </a>

            <!-- links -->
            <ul id="main_nav">
                <li v-for="link, i in mainNavLinks" :key="i">
                    <a :href="link.href">
                        <img
                            v-if="link.img != null"
                            :src="require(`../assets${link.img}`)" 
                            :alt="link.text"
                        >
                        {{ link.text }}
                    </a>
                </li>
            </ul>

            <!-- cart and search -->
            <ul id="rigth_nav">
                <li v-for="link, i in rigthNavLinks" :key="i">
                    <a :href="link.href">
                        <img
                            v-if="link.img != null"
                            :src="require(`../assets${link.img}`)" 
                            :alt="link.text"
                        >
                        {{ link.text }}
                    </a>
                </li>
            </ul>
        </nav>
        <section id="jumbotron">
            <img src="../assets/img/jumbo/h3-rev-img-5.png" alt="">
            <img src="../assets/img/jumbo/h3-rev-img-6.png" alt="">
        </section>
    </header>
</template>

<script>
export default {
    name: 'AppHeader',
    props: {
        mainNavLinks:Array,
        rigthNavLinks:Array
    }
}
</script>

<style lang="scss" scoped>
header {
    background-color: #181818;
    text-transform: uppercase;
    padding-bottom: 150px;

    a {
        color: white;
    }

    nav {
        width: 80%;
        margin: 0 auto;
        padding: 20px 0;
        // flex
        display: flex;
        justify-content: space-between;
        align-items: center;

        ul {
            display: flex;
            align-items: center;

            li {
                margin-right: 30px;

                img {
                    height: 120px;
                }
            }

            li:last-of-type {
                margin: 0;
            }
        }

        #rigth_nav {

            img {
                height: 20px;
                filter: invert(1);
            }
        }
    }

    #jumbotron {
        text-align: center;
        position: relative;

        img:last-of-type {
            position: absolute;
            top: 62%;
            left: 50%;
            transform: translate(-50%, -50%);
        }
    }
}
</style>>
