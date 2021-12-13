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

</style>>
