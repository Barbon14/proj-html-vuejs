<template>
    <main>
        <section>
            <img 
                class="thumb"
                v-for="thumb, i in thumbs" :key="i"
                :src="require(`../assets/img/jumbo/${thumb}`)" 
                alt=""
            >
        </section>
    </main>
</template>

<script>
export default {
    name: 'AppMain',
    props: {
        thumbs: Array
    }
}
</script>
    
<style lang="scss" scoped>
main {

    .thumb {
        width: calc(25% - 10px);
        margin: 0 5px;
    }
}
</style>