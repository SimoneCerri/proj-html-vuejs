<script>
import CenterHeaderSlot from "./HeaderComponents/CenterHeaderSlot.vue"

export default {
    name: "Header",
    components:
    {
        CenterHeaderSlot,
    },
    data() {
        return {
            headerSlots:
                [
                    "Home",
                    "About",
                    "Portfolio",
                    "Our Process",
                    "Pricing",
                    "Blog",
                    "Contact"
                ]
        }
    }
}
</script>

<template>
    <CenterHeaderSlot v-for="slot in headerSlots" :name="slot"></CenterHeaderSlot>
</template>

<style scoped>

</style>