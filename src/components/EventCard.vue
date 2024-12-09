<template>
    <div class="my-component">
        <span>@{{ event.time }} on {{ event.date }}</span>
        <h4>{{ event.title }}</h4>
        <BaseIcon name="users" />
        <span>{{ event.attendees.length }} attending</span>
    </div>
</template>

<script lang="ts">
export default {
    props: {
        event: Object,
    },
}
</script>

<style lang="scss" scoped>
.my-component {
    h4 {
        color: $blue;
    }

    .quadrado {
        width: 100px;
        height: 100px;
        background: blue;
    }
}
</style>
