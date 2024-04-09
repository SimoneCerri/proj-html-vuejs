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
        </div>
        <div class="card_title">
            {{ card.title || card.number }}
        </div>
        <div class="card_info">
            {{ card.info || card.name }}
        </div>
    </div>
</template>

<style scoped>

</style>
