<script>
export default {
    name: "CardImage",
    props:
    [
        "image",
    ],
    mounted()
    {
        console.log(this.image);
    }
}
</script>

<template>
    <div class="card_image">
        <img :src="image" alt="">
    </div>
</template>

<style scoped></style>