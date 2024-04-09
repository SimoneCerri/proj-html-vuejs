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
                ],
                src:"./img/footer-logo.png"
        }
    }
}
</script>

<template>
    <div class="top container little_space">
        <Logo :src />
        <div class="footer_info">
            <TopFooter v-for="slot in footerSlots" :name="slot"></TopFooter>
        </div>
    </div>
    <hr class="container hr">
    <div class="bottom container little_space">
        <BottomFooter></BottomFooter>
    </div>
</template>

<style scoped></style>