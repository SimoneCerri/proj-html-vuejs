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
                        icon: "./img/smart1.png",
                        title: "3D modeling",
                        info: "We constantly ask questions. It helps us hsape your story and deliver the results you crave. Yep, we'll drill deep to deliver above and beyond your expectations.",
                    },
                    {
                        icon: "./img/smart2.png",
                        title: "Collaboration",
                        info: "We constantly ask questions. It helps us hsape your story and deliver the results you crave. Yep, we'll drill deep to deliver above and beyond your expectations.",
                    },
                    {
                        icon: "./img/smart3.png",
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
            members:
                [
                    {
                        icon: "./img/team1.png",
                        title: "Robert Coleman",
                        info: "Owner & Creative Director",
                    },
                    {
                        icon: "./img/team2.png",
                        title: "Don Woods",
                        info: "Administrator",
                    },
                    {
                        icon: "./img/team4.png",
                        title: "Tomas Nash",
                        info: "2d animator & Compositor",
                    },
                ],
            clientsCards:
                [
                    "./img/sponsor1.png",
                    "./img/sponsor2.png",
                    "./img/sponsor3.png",
                    "./img/sponsor4.png",
                    "./img/sponsor5.png",
                    "./img/sponsor6.png",
                ],
            tipButton: "Submit",
        }
    }
}
</script>

<template>
    <div id="main">
        <!-- ##################################################### -->
        <!-- ## Can be refactoring with a V-FOR to make section ## -->
        <!-- ## with h3/h1/h5 + V-FOR for cards + V-IF="button" ## -->
        <!-- ##################################################### -->

        <!-- ##################################################### -->
        <!-- ## Can move each section as a component for better ## -->
        <!-- ## maintenance of the App/Site , if have time left ## -->
        <!-- ##################################################### -->

        <section class="slogan spacing">
            <div class="up_shape"></div>
            <div class="prova"></div>
            <div class="moon1"></div>
            <div class="ship"></div>
            <div class="stars1"></div>
            <div class="stars2"></div>
            <h3 class="danger">
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
            <h4 class="">
                We are a character-driven animation studio striving to make high-quality animations.
            </h4>
            <div class="moon2"></div>
            <div class="df just_center align_center btn_middle spacing">
                <Button v-for="button in Buttons" :name="button"></Button>
            </div>
            <div class="slogan_video container little_space">
                <CardImage :src="imageSlogan" />
                <div class="play">
                    <a href=""><i class="fa-solid fa-play"></i></a>
                </div>
            </div>
            <div class="man1"></div>
            <div class="man2"></div>
        </section>
        <!-- /.slogan -->
        <section class="animation_love spacing">
            <div class="vr_man"></div>
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
            <h5>
                Our culture inspires the creative and innovative spirit found throughout our Studio. We breath life into
                new ideas !
            </h5>
            <div class="our_skills_cards container spacing">
                <CardWithInfo v-for="card in ourSkills" :card class="card_love" />
            </div>
            <div class="ship"></div>
        </section>
        <!-- /.animation_love -->
        <section class="quick_facts spacing">
            <div class="up_shape">

            </div>
            <h1>
                Anidio Quick Facts
            </h1>
            <div class="our_anidio_cards container spacing">
                <CardWithInfo v-for="card in audioCards" :card />
            </div>
            <div class="moon"></div>
        </section>
        <!-- /.quick_facts -->
        <section class="our_works spacing">
            <h3>
                Our Works
            </h3>
            <h1 class="little_space">
                Featured Productions
            </h1>
            <h5>
                Here's just a small sample of some of those projects that we're quite proud of.
            </h5>
            <h5>
                If you're looking for something specific feel free to get in contact with us.
            </h5>
            <div class="our_works_cards container spacing">
                <CardImage v-for="card in ourWorksCards" :src="card" />
            </div>
            <div class="space_bottom">
                <Button :name="ourWorkButton" />
            </div>
        </section>
        <!-- /.our_works -->
        <section class="our_process spacing container">
            <div class="left">

            </div>
            <div class="right">
                <h3>
                    Our Process
                </h3>
                <h1>
                    Our Process for Your Animation Production
                </h1>
                <h5>
                    We have an effetctive process for working on animation
                </h5>
                <div class="our_process_cards spacing">
                    <CardWithInfo v-for="card in cardProcess" :card />
                </div>
                <div class="buttons">
                    <div class="left_arrow">
                        <i class="fa-solid fa-arrow-left"></i>
                    </div>
                    <div class="right_arrow">
                        <i class="fa-solid fa-arrow-right"></i>
                    </div>
                </div>
            </div>
            <div class="ship"></div>
        </section>
        <!-- /.our_process -->
        <section class="members spacing">
            <div class="moon1"></div>
            <div class="moon2"></div>
            <div class="moon3"></div>
            <h3>
                Anidio Magic Team Member
            </h3>
            <h1 class="little_space">
                Let Us Animate Your Project
            </h1>
            <h5>
                We create new worlds! Let's collaborate and create engaging, effective, award-winning animations.
            </h5>
            <div class="members_cards container spacing">
                <CardWithInfo v-for="card in members" :card />
            </div>
            <div class="buttons">
                <div class="left_arrow">
                    <i class="fa-solid fa-arrow-left"></i>
                </div>
                <div class="right_arrow">
                    <i class="fa-solid fa-arrow-right"></i>
                </div>
            </div>
        </section>
        <!-- /.members -->
        <section class="clients spacing">
            <h3>
                Why Anidio studio ?
            </h3>
            <h1 class="little_space">
                We Love Our Clients
            </h1>
            <h5>
                We are trusted throughout adland and have a wealth of recommendations from start-ups to renowned global
                brands.
            </h5>
            <div class="clients_cards container spacing">
                <CardImage v-for="src in clientsCards" :src />
            </div>
        </section>
        <!-- /.clients -->
        <section class="tips spacing">
            <div class="up_shape">

            </div>
            <h3>
                We Create New Worlds !
            </h3>
            <h1 class="little_space">
                Want Tips On Your Storytelling ?
            </h1>
            <h5>
                Join our neswletter for tips on how to elevate your brand through storytelling
            </h5>
            <form action="submit" class="spacing">
                <input type="text" placeholder="Enter your email">
                <div class="button">
                    <Button :name="tipButton" />
                </div>
            </form>
            <div class="bottom_shape"></div>
        </section>
        <!-- /.tips -->
    </div>
</template>

<style scoped>
.btn_middle {
    gap: 1em;
}
</style>