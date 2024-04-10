<script>
export default {
    name: "TopFooter",
    props: ["name"]
}
</script>

<template>
    <div>{{ name }}</div>
</template>

<style scoped>
div:hover
{
    color: var(--danger);
}
</style>