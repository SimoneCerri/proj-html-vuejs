<script>
export default {
    name: "CenterHeader",
    props:["name"]
}
</script>

<template>
    <div class="index">{{ name }}</div>
</template>

<style scoped>
.index
{
    z-index: 9999;
}
</style>