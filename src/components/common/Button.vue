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
    background-color: var(--light);
}

:hover {
    cursor: pointer;
    color: var(--lightest);
    border-color: var(--lightest);
    box-shadow: 0px 2px 2px 0px var(--lightest);
    background-color: var(--primary);
}
</style>