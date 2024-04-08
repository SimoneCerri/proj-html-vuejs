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
    <div id="header" class="container">
        <LeftHeader></LeftHeader>
        <div class="center_header">
            <CenterHeader v-for="slot in headerSlots" :name="slot" class="CenterHeader"></CenterHeader>
        </div>
        <RightHeader></RightHeader>
    </div>
</template>

<style>

</style>