<script>
import Logo from "../common/Logo.vue"
export default {
    name: "LeftHeader",
    components:
    {
        Logo,
    },
    data() {
        return {
            src:"./img/logo.png"
        }
    }
}
</script>

<template>
    <Logo :src />
</template>

<style scoped>

</style>