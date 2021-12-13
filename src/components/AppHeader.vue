<template>
    <header>
        <nav>
            <!-- order online -->
            <a href="#" class="btn">
                
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

        ul {
            display: flex;
            align-items: center;

            li {
                margin: 0 20px;

                img {
                    height: 120px;
                }
            }
        }

        #rigth_nav {

            img {
                height: 20px;
                filter: invert(1);
            }
        }
    }
}
</style>>
