<script>
export default {
    name: "Button",
    props:
    [
        "name",
    ]
}
</script>

<template>
    <button class="my_btn">
        {{ name }}
    </button>
</template>

<style scoped>
:hover
{
    cursor: pointer;
}
</style>