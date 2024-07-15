<script setup>
defineProps({
    title: {
        type: String,
        required: true,
    },
});

</script>

<template>
    <div class="Card">
        <h1>{{ title }}</h1>
        <slot></slot>
    </div>
</template>

<style scoped>
.Card {
    padding: 20px;
    border: 1px solid gray;
    border-radius: 5px;
    box-shadow: 3px 3px 2px 2px gray;
}
</style>