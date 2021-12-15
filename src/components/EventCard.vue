<template>
    <div class="event_card">
        <div>
            {{ event.day }}
        </div>
        <div>
            {{ event.month }}
        </div>
        <h3>
            {{ event.name }}
        </h3>
        <h6>
            <i class="fas fa-map-marker-alt"></i>
            {{ event.address }}
        </h6>
    </div>
</template>

<script>
export default {
    name: 'EventCard',
    props: {
        event: Object
    }
}
</script>

<style lang="scss" scoped>

</style>
