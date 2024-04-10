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
.my_btn
{
    border: 1px solid transparent;
}

:hover {
    cursor: pointer;
    background-color: var(--primary);
    color: var(--lightest);
    border-color: var(--lightest);
    box-shadow: 0px 2px 2px 0px var(--lightest);
}
</style>