<script>
import CenterHeader from "./HeaderComponents/CenterHeader.vue"
import LeftHeader from "./HeaderComponents/LeftHeader.vue"
import RightHeader from "./HeaderComponents/RightHeader.vue"


export default {
    name: "Header",
    components:
    {
        CenterHeader,
        LeftHeader,
        RightHeader
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
    <section class="header">
        <div id="header" class="container">
            <LeftHeader></LeftHeader>
            <div class="center_header">
                <div class="moon">

                </div>
                <CenterHeader v-for="slot in headerSlots" :name="slot"></CenterHeader>
            </div>
            <RightHeader></RightHeader>
        </div>
    </section>
</template>

<style scoped></style>