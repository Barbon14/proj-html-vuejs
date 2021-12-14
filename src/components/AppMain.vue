<template>
    <main>
        <section>
            <img
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

</style>