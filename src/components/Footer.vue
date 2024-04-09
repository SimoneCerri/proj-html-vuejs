<script>
import TopFooter from "./FooterComponents/TopFooter.vue"
import BottomFooter from "./FooterComponents/BottomFooter.vue"
import Logo from "./common/Logo.vue"

export default {
    name: "Footer",
    components:
    {
        TopFooter,
        BottomFooter,
        Logo,
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
    <div class="top container spacing">
        <Logo />
        <div class="footer_info">
            <TopFooter v-for="slot in footerSlots" :name="slot"></TopFooter>
        </div>
    </div>
    <hr class="container hr">
    <div class="bottom container spacing">
        <BottomFooter></BottomFooter>
    </div>
</template>

<style scoped></style>