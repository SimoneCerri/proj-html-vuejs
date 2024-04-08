<script>
import Button from "../common/Button.vue"

export default {
    name: "RightHeader",
    components:
    {
        Button,
    },
    data()
    {
        return{
            buttonText:"Get a Quote"
        }
    }
}
</script>

<template>
    <Button :name="buttonText"></Button>
</template>

<style scoped>
.my_btn
{
    background-color: var(--light);
}
</style>