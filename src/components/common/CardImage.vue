<script>
export default {
    name: "CardImage",
    props:
    [
        "src",
    ],
    mounted()
    {
        //console.log(this.src);
    }
}
</script>

<template>
    <div class="card_image">
        <img :src alt="">
    </div>
</template>

<style scoped>

</style>