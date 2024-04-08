<script>
import Button from "./common/Button.vue"
import CardImage from "./common/CardImage.vue"
import CardWithInfo from "./common/CardWithInfo.vue"

export default {
    name: "Main",
    components:
    {
        Button,
        CardImage,
        CardWithInfo,
    },
    data() {
        return {
            Buttons:
                [
                    "Start a Project",
                    "Portfolio"
                ],
            imageSlogan: "./img/middle.png",
            ourSkills:
                [
                    {
                        icon: "fa-brands fa-searchengin",
                        title: "3D modeling",
                        info: "We constantly ask questions. It helps us hsape your story and deliver the results you crave. Yep, we'll drill deep to deliver above and beyond your expectations.",
                    },
                    {
                        icon: "fa-solid fa-arrows-spin",
                        title: "Collaboration",
                        info: "We constantly ask questions. It helps us hsape your story and deliver the results you crave. Yep, we'll drill deep to deliver above and beyond your expectations.",
                    },
                    {
                        icon: "fa-solid fa-brain",
                        title: "Creativity",
                        info: "We constantly ask questions. It helps us hsape your story and deliver the results you crave. Yep, we'll drill deep to deliver above and beyond your expectations.",
                    },
                ]
        }
    }
}
</script>

<template>
    <div id="main">
        <section class="slogan spacing">
            <h3>
                Imagine,Create,Experience
            </h3>
            <div class="little_space">
                <h1>
                    We Animate
                </h1>
                <h1>
                    With Ninja-Like Precision
                </h1>
            </div>
            <h3>
                We are a character-driven animation studio striving to make high-quality animations.
            </h3>
            <div class="df just_center align_center btn_middle spacing">
                <Button v-for="button in Buttons" :name="button"></Button>
            </div>
            <div class="slogan_video container">
                <CardImage :src="imageSlogan" />
                <div class="play">
                    <a href=""><i class="fa-solid fa-play"></i></a>
                </div>
            </div>
        </section>
        <!-- /.slogan -->
        <section class="animation_love spacing">
            <h3>
                Our Love For Animation
            </h3>
            <h1 class="little_space">
                We're StoryTelling Expert With Creative Smarts
            </h1>
            <h4>
                Our culture inspires the creative and innovative spirit found throughout our Studio. We breath life into
                new ideas !
            </h4>
            <div class="our_skills_cards container spacing">
                <CardWithInfo v-for="card in ourSkills" :card />
            </div>
        </section>
        <!-- /.animation_love -->
        <section class="quick_facts spacing">

        </section>
        <!-- /.quick_facts -->
        <section class="our_works spacing">

        </section>
        <!-- /.our_works -->
        <section class="our_process spacing">

        </section>
        <!-- /.our_process -->
        <section class="members spacing">

        </section>
        <!-- /.members -->
        <section class="clients spacing">

        </section>
        <!-- /.clients -->
        <section class="tips spacing">

        </section>
        <!-- /.tips -->
    </div>
</template>

<style scoped>
.btn_middle {
    gap: 1em;
}
</style>