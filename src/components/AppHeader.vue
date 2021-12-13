<template>
    <header>
        <nav>
            <!-- order online -->
            <a href="#" class="btn">

            </a>

            <!-- links -->
            <ul>
                <li v-for="link, i in navLinks" :key="i">
                    <a :href="link.href">
                        <img
                            v-if="link.img != null"
                            :src="require(`../assets/img/logos/${link.img}`)" 
                            alt=""
                        >
                        {{ link.text }}
                    </a>
                </li>
            </ul>

            <!-- cart and search -->
            <ul>
                <li>
                    <a href="#">
                        <img src="" alt="">

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
        navLinks:Array
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
    }
}
</style>>
