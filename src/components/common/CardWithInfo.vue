<script>
export default {
    name: "CardWithInfo",
    props: {card:Object},
    mounted()
    {
        //console.log(this.card.icon);
    }
}
</script>

<template>
    <div class="card">
        <div class="card_icon">
            <i :class=card.icon></i>
            <img :src=card.icon alt="">
        </div>
        <div class="card_title">
            {{ card.title || card.number }}
        </div>
        <div class="card_info">
            {{ card.info || card.name }}
        </div>
        <div class="socials">
            <div class="facebook">
                <a href="">
                    <i class="fa-brands fa-facebook-f"></i>
                </a>
            </div>
            <div class="twitter">
                <a href="">
                    <i class="fa-brands fa-twitter"></i>
                </a>
            </div>
            <div class="instagram">
                <a href="">
                    <i class="fa-brands fa-instagram"></i>
                </a>
            </div>
        </div>
    </div>
</template>

<style scoped>

</style>
