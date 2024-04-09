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
            /* ######################################################### */
            /* ## ALL THAT DATA CAN BE PLACED IN A STORE.JS MAYBE (?) ## */
            /* ######################################################### */
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
                ],
            audioCards:
                [
                    {
                        number: "700+",
                        name: "Projects done",
                    },
                    {
                        number: "250+",
                        name: "Happy Clients",
                    },
                    {
                        number: "25+",
                        name: "Team Members",
                    },
                    {
                        number: "12+",
                        name: "Years on the market",
                    },
                ],
            ourWorksCards:
                [
                    "./img/work1.png",
                    "./img/work2.png",
                    "./img/work3.png",
                    "./img/work4.png",
                ],
            ourWorkButton: "See Our Work",
            cardProcess:
                [
                    {
                        icon: "./img/process1.png",
                        title: "Pre-Production",
                        info: "We'll take your idea and create technical script which consists of action notes and animation descriptions",
                    },
                    {
                        icon: "./img/process2.png",
                        title: "Scripting",
                        info: "We'll take your idea and create technical script which consists of action notes and animation descriptions",
                    },
                ],
        }
    }
}
</script>

<template>
    <div id="main">
        <!-- ##################################################### -->
        <!-- ## can be refactoring with a V-FOR to make section ## -->
        <!-- ## with h3/h1/h4 + V-FOR for cards + V-IF="buttons" ##-->
        <!-- ##################################################### -->
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
            <div class="little_space">
                <h1>
                    We're StoryTelling
                </h1>
                <h1>
                    Expert With Creative Smarts
                </h1>
            </div>
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
            <h1>
                Anidio Quick Facts
            </h1>
            <div class="our_anidio_cards container spacing">
                <CardWithInfo v-for="card in audioCards" :card />
            </div>
        </section>
        <!-- /.quick_facts -->
        <section class="our_works spacing">
            <h3>
                Our Works
            </h3>
            <h1 class="spacing">
                Featured Productions
            </h1>
            <h4>
                Here's just a small sample of some of those projects that we're quite proud of.
            </h4>
            <h4>
                If you're looking for something specific feel free to get in contact with us.
            </h4>
            <div class="our_works_cards container spacing">
                <CardImage v-for="card in ourWorksCards" :src="card" />
            </div>
            <Button :name="ourWorkButton" />
        </section>
        <!-- /.our_works -->
        <section class="our_process spacing container">
            <div class="left">
                <img src="../../img/process-thumb.png" alt="">
            </div>
            <div class="right">
                <h3>
                    Our Process
                </h3>
                <h1>
                    Our Process for Your Animation Production
                </h1>
                <h4>
                    We have an effetctive process for working on animation
                </h4>
                <div class="our_process_cards spacing">
                    <CardWithInfo v-for="card in cardProcess" :card />
                </div>
                <div class="buttons">
                    <div class="arrow">
                        <i class="fa-solid fa-arrow-left"></i>
                    </div>
                    <div class="arrow">
                        <i class="fa-solid fa-arrow-right"></i>
                    </div>
                </div>
            </div>
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