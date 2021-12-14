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
        <section id="testimonials">
            <div>
                <h2>
                    "
                </h2>
                <h3>
                    "forget the trendy pizza shops, this hidden spot makes the best new york-style pizza slice in naples"
                </h3>
                <h5>
                    washington post 2018
                </h5>
            </div>
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

    #testimonials {
        background-image: url('../assets/img/h3-testimonials-bckgrnd.jpg');
        height: 495px;
    }
}
</style>