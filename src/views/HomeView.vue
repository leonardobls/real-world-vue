<template>
    <div class="home">
        <EventCard v-for="event in events" :key="event.id" :event="event" />
    </div>
</template>

<script>
// @ is an alias to /src
import EventCard from '@/components/EventCard.vue'
import EventService from '@/services/EventService.js'

export default {
    components: {
        EventCard,
    },

    data() {
        return {
            events: [],
        }
    },

    created() {
        EventService.getEvents
            .then((response) => {
                this.events = response.data
            })
            .catch((error) => {
                console.log(`There was an error: ${error.response}`)
            })
    },
}
</script>
