<template>
<div class="about-hero">
    <img class="texture-1-icon" alt="" src="../assets/texture/texture.png" />
    <img class="green-and-purple-upscaled-1-icon" alt="" src="../assets/texture/green-and-purple-upscaled.png" />
    <img class="texture-2-icon" alt="" src="../assets/texture/texture.png" />
    <div class="hey-im-basab">HEY, I'M BASAB</div>
    <div class="hey-im-basab2">HEY, I'M BASAB</div>
    <div class="hey-im-basab1">HEY, I'M BASAB</div>
    <img class="about-hero-child" alt="" src="../assets/texture/line1.png" />
    <div class="scroll">scroll</div>
</div>
</template>

<script>
import {
    defineComponent
} from "vue";
import {
    gsap
} from "gsap";
export default defineComponent({
    name: "AboutHero",
    mounted() {
      gsap.from(".hey-im-basab", {
      duration: 1,
      x: -100, // Slide from left to right
      opacity: 0,
      delay:0.8, 
      ease: "power2.out", 
    });

    gsap.from(".hey-im-basab1", {
      duration: 1,
      x: 100, // Slide from right to left
      opacity: 0, 
      ease: "power2.out", 
      delay: 0.8, 
    });

    gsap.from(".hey-im-basab2", {
      duration: 1,
      y: -50, // Slide from top to bottom
      opacity: 0, 
      ease: "power2.out", 
      delay: 0.8, 
    });
    gsap.from(".scroll", {
      duration: 1,
      y: -50, // Slide from top to bottom
      opacity: 0, 
      ease: "power2.out", 
      delay: 0.2, 
      scrollTrigger: {
                trigger: ".scroll",
                start: "top 80%",
                end: "bottom 60%",
            },
    });

    gsap.from(".texture-1-icon", { duration: 1, scale: 0, opacity: 0, ease: "power2.out", delay:0.8 });
    gsap.from(".green-and-purple-upscaled-1-icon", { duration: 1, y: -100, opacity: 0, ease: "power2.out", delay: 0.8 });
    gsap.from(".texture-2-icon", { duration: 1, x:-100, opacity: 0, ease: "power2.out", delay: 0.8 });
    }
});
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@300;900&display=swap");

body {
    margin: 0;
    line-height: normal;
}

.texture-1-icon {
    position: absolute;
    top: 0px;
    left: 970px;
    width: 470px;
    height: 466px;
    object-fit: cover;
}

.green-and-purple-upscaled-1-icon {
    position: absolute;
    top: 138px;
    left: 0px;
    width: 276px;
    height: 662px;
    object-fit: cover;
}

.texture-2-icon {
    position: absolute;
    top: 258px;
    left: 138px;
    width: 1102px;
    height: 414px;
    object-fit: cover;
}

.hey-im-basab {
    position: absolute;
    top: 138px;
    left: 170px;
    font-weight: 900;
    display: flex;
    align-items: center;
    justify-content: center;
    width: 1100px;
    height: 154px;
}

.hey-im-basab1 {
    position: absolute;
    top: 465px;
    left: 170px;
    font-weight: 900;
    display: flex;
    align-items: center;
    justify-content: center;
    width: 1100px;
    height: 154px;
}

.hey-im-basab2 {
    position: absolute;
    top: 292px;
    left: 225px;
    font-weight: 900;
    color: rgba(0, 0, 0, 0);
    -webkit-text-stroke-width: 4px;
    -webkit-text-stroke-color: rgb(255, 255, 255);
    display: flex;
    align-items: center;
    justify-content: center;
    width: 989px;
    font-family: Inter;
}

.about-hero-child {
    position: absolute;
    top: 725px;
    left: 1410px;
    width: 0px;
    height: 58px;
    object-fit: contain;
}

.scroll {
    position: absolute;
    top: 629px;
    left: 1360px;
    font-size: 20px;
    letter-spacing: 0.3em;
    font-weight: 300;
    transform: rotate(90deg);
    transform-origin: 0 0;
}

.about-hero {
    position: relative;
    background-color: #000;
    width: 100%;
    height: 800px;
    overflow: hidden;
    text-align: center;
    font-size: 128px;
    color: #fff;
    font-family: Inter;
}
</style>
