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
            <i class="fas fa-quote-left"></i>
            <h3>
                "forget the trendy pizza shops, this hidden spot makes the best new york-style pizza slice in naples"
            </h3>
            <h6>
                washington post 2018
            </h6>
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
}
</style>