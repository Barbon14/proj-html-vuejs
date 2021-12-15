<template>
    <div class="event_card">
        <span class="date">
            <h2 class="event_day text_brown">
                {{ event.day }}
            </h2>
            <h3>
                {{ event.month }}
            </h3>
        </span>
        <span>
            <h3>
                {{ event.name }}
            </h3>
            <h6 class="text_brown">
                <i class="fas fa-map-marker-alt"></i>
                {{ event.address }}
            </h6>
        </span>
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
.event_card {
    display: flex;
    border-bottom: 2px dotted #b7903c;
    padding: 30px 0;

    .date {
        text-align: center;
        margin-right: 20px;
        line-height: 42px;
    }

    .event_day {
        font-size: 45px;
    }
}
</style>
