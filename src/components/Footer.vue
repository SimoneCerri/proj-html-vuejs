<script>
import TopFooter from "./FooterComponents/TopFooter.vue"
import BottomFooter from "./FooterComponents/BottomFooter.vue"

export default {
    name: "Footer",
    components:
    {
        TopFooter,
        BottomFooter
    },
    data() {
        return {
            footerSlots:
                [
                    "About Us",
                    "Portfolio",
                    "Pricing",
                    "Career",
                    "Contact"
                ]
        }
    }
}
</script>

<template>
    <TopFooter v-for="slot in footerSlots" :name="slot"></TopFooter>
    <BottomFooter></BottomFooter>
</template>

<style scoped></style>