<template>
    <div class="team_card">
        <img :src="require(`../assets/img/team/${mate.pic}`)" :alt="mate.name">
        <div class="mate_info">
            <h2>
                {{ mate.name }}
            </h2>
            <div class="role">
                {{ mate.role}}
            </div>
            <div class="social">
                <a :href="mate.instagram">
                    <i class="fab fa-instagram"></i>
                </a>
                <a :href="mate.twitter">
                    <i class="fab fa-twitter"></i>
                </a>
                <a :href="mate.facebook">
                    <i class="fab fa-facebook-f"></i>
                </a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'TeamCard',
    props: {
        mate: Object
    }
}
</script>

<style lang="scss" scoped>
.team_card {
    position: relative;
    width: 25%;
    color: white;
    
    a {
        color: white;
    }

    img {
        width: 100%;
        height: 100%;
    }

    .mate_info {
        display: none;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        width: 100%;
        height: 100%;
        background-color: #ca3e12;
        position: absolute;
        top: 0;
        left: 0;
        border: 30px solid whitesmoke;

        .role{
            text-transform: capitalize;
        }

        .social {
            .fab {
                margin: 5px;
            }
        }
    }

    &:hover .mate_info{
        display: flex;
    }
}
</style>
