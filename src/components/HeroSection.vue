<template>
<div class="hero-section">
    <img class="texture-3-icon" alt="" src="../assets/texture/texture.png" />
    <img class="green-1-icon" alt="" src="../assets/texture/green.png" />
    <b class="i-craft-immersive">I craft immersive digital journeys that seamlessly blend development with
        captivating design.</b>

    <div class="animate">
        <b class="about-me">about me.</b>
    <img class="hero-section-child" alt="" src="../assets/texture/line2.png" />
    <img class="avatar-1-icon" alt="" src="../assets/avatar.png" />
    <b class="a-brief-intro">A brief intro, who am I?</b>
    <div class="i-am-a-container">
        <span class="i-am-a-container1">
            <p class="i-am-a">
                I am a passionate Fullstack Web Developer and UI/UX Designer rooted in
                Kathmandu, Nepal.
            </p>
            <p class="i-am-a">&nbsp;</p>
            <p class="i-am-a">
                With a blend of technical expertise and creative design, I craft
                digital experiences that bridge functionality with aesthetic appeal.
            </p>
            <p class="i-am-a">&nbsp;</p>
            <p class="i-am-a">
                When I am not developing or designing, I enjoy creating video content
                that talk about frontend development and design on YouTube
            </p>
        </span>
    </div>

    </div>
</div>
</template>

  
<script>
import {
    defineComponent
} from "vue";
import {
    gsap
} from "gsap";
import {
    ScrollTrigger
} from "gsap/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);

export default defineComponent({
    name: "HeroSection",
    mounted() {
        gsap.from(".texture-3-icon", {
            duration: 1.5,
            scale: 0,
            opacity: 0,
            ease: "power2.out",
            scrollTrigger: {
                trigger: ".texture-3-icon",
                start: "top 80%",
                end: "bottom 60%",
            },
        });

        gsap.from(".green-1-icon", {
            duration: 1.5,
            x: 200,
            opacity: 0,
            ease: "power2.out",
            scrollTrigger: {
                trigger: ".green-1-icon",
                start: "top 80%",
                end: "bottom 80%",
            },
        });

        gsap.from(".i-craft-immersive", {
            duration: 1,
            y: 50,
            opacity: 0,
            ease: "power2.out",
            scrollTrigger: {
                trigger: ".i-craft-immersive",
                start: "top 80%",
                end: "bottom 60%",
                scrub: true,
            },
        });

        gsap.from(".animate", {
            duration: 1,
            x: 200,
            opacity: 0,
            ease: "power2.out",
            scrollTrigger: {
                trigger: ".about-me",
                start: "top 80%",
                end: "bottom 80%",
            },
        });

    },
});
</script>
  
<style scoped>
.texture-3-icon {
    position: absolute;
    top: 86px;
    left: 0px;
    width: 149px;
    height: 624px;
    object-fit: cover;
}

.green-1-icon {
    position: absolute;
    top: 398px;
    left: 784px;
    width: 656px;
    height: 64px;
    object-fit: cover;
}

.i-craft-immersive {
    position: absolute;
    top: 106px;
    left: 60px;
    display: flex;
    align-items: center;
    width: 1332px;
    height: 292px;
}

.about-me {
    position: absolute;
    top: 730px;
    left: 480px;
    font-size: 96px;
    text-align: center;
}

.hero-section-child {
    position: absolute;
    top: 846px;
    left: 386px;
    max-height: 100%;
    width: 668.05px;
    object-fit: cover;
}

.avatar-1-icon {
    position: absolute;
    top: 929px;
    left: 132px;
    width: 400px;
    height: 400px;
    object-fit: cover;
}

.a-brief-intro {
    position: absolute;
    top: 929px;
    left: 607px;
    font-size: 40px;
    display: flex;
    align-items: center;
    width: 460px;
    height: 72px;
}

.i-am-a {
    margin: 0;
}

.i-am-a-container1 {
    width: 100%;
}

.i-am-a-container {
    position: absolute;
    top: 1001px;
    left: 607px;
    font-size: 28px;
    font-weight: 200;
    color: #fff;
    display: flex;
    align-items: center;
    width: 713px;
}

.hero-section {
    position: relative;
    background-color: #000;
    width: 100%;
    height: 1460px;
    overflow: hidden;
    text-align: left;
    font-size: 64px;
    color: rgba(255, 255, 255, 0.8);
    font-family: Inter;
}
</style>
