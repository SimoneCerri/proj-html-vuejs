<script>
import Button from "./common/Button.vue"
import CardImage from "./common/CardImage.vue"

export default {
    name: "Main",
    components:
    {
        Button,
        CardImage,
    },
    data()
    {
        return{
            Buttons:
            [
                "Start a Project",
                "Portfolio"
            ],
            imageSlogan:"./img/middle.png"
        }
    }
}
</script>

<template>
    <div id="main">
        <section class="slogan">
            <h3>
                Imagine,Create,Experience
            </h3>
            <h1>
                We Animate With Ninja-Like Precision
            </h1>
            <h3>
                We are a character-driven animation studio striving to make high-quality animations.
            </h3>
            <Button v-for="button in Buttons" :name="button"></Button>
            <CardImage :src="imageSlogan" />
        </section>
        <!-- /.slogan -->
        <section class="animation_love">

        </section>
        <!-- /.animation_love -->
        <section class="quick_facts">

        </section>
        <!-- /.quick_facts -->
        <section class="our_works">

        </section>
        <!-- /.our_works -->
        <section class="our_process">

        </section>
        <!-- /.our_process -->
        <section class="members">

        </section>
        <!-- /.members -->
        <section class="clients">

        </section>
        <!-- /.clients -->
        <section class="tips">

        </section>
        <!-- /.tips -->
    </div>
</template>

<style scoped></style>