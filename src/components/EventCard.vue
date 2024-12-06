<template>
    <div class="my-component">
        <h4>{{ title }}</h4>
        <div class="quadrado"></div>
    </div>
</template>

<script lang="ts">
export default {
    data() {
        return {
            title: 'Park Cleanup',
        }
    },
}
</script>

<style lang="scss" scoped>
.my-component {
    background: red;
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
