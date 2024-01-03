<template>
<div class="service-section">
    <img class="texture-4-icon" alt="" src="../assets/texture/texture.png" />
    <b class="services">services.</b>
    <i class="my-expertise">my expertise.</i>
    <i class="web-developmentfrontendbacke">Web Development(Frontend/Backend)
    </i>
    <i class="web-design">Web Design</i>
    <i class="uiux-design">UI/UX Design</i>
    <div class="i-specialise-in">
        I specialise in everything web-design, seamlessly merging development and
        design to create captivating digital experiences. My goal is to innovate
        and elevate every project, ensuring user-centric design and top-notch
        functionality across the web landscape.
    </div>
    <div class="stack">
        <i class="my-digital-toolbox">my digital toolbox.</i>
    <img class="mongodb-icon-1" alt="" src="../assets/tech-stack/mongodb-icon.png" />
    <img class="django-icon-1" alt="" src="../assets/tech-stack/django-icon.png" />
    <img class="vue-js-icon-1" alt="" src="../assets/tech-stack/vue-js-icon.png" />
    <img class="nuxt-js-icon-1" alt="" src="../assets/tech-stack/nuxt-js-icon.png" />
    <img class="tailwind-css-icon-1" alt="" src="../assets/tech-stack/tailwind-css-icon.png" />
    <img class="node-js-icon-1" alt="" src="../assets/tech-stack/node-js-icon.png" />
    <img class="figma-icon-1" alt="" src="../assets/tech-stack/figma-icon.png" />

    </div>
</div>
</template>

  
<script>
import { defineComponent } from "vue";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
gsap.registerPlugin(ScrollTrigger);


export default defineComponent({
  name: "ServiceSection",
  mounted() {
    // Texture animation
    gsap.from(".texture-4-icon", {
      duration: 1.5,
      x:100,
      scale: 0,
      opacity: 0,
      ease: "slide.out",
      scrollTrigger: {
                trigger: ".service-section",
                start: "top 80%",
                end: "bottom 60%",
            },
    });

    gsap.from(".services, .my-expertise, .stack, .web-developmentfrontendbacke, .web-design, .uiux-design, .i-specialise-in, .my-digital-toolbox", {
      duration: 1,
      opacity: 0,
      ease: "power2.out",
      scrollTrigger: {
                trigger: ".service-section",
                start: "top 80%",
                end: "bottom 60%",
            },
    });
  },
});
</script>

  
<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Inter:ital,wght@0,300;0,700;1,700&display=swap");

body {
    margin: 0;
    line-height: normal;
}

.texture-4-icon {
    position: absolute;
    top: 0px;
    left: 1190px;
    width: 202px;
    height: 454px;
    object-fit: cover;
}

.services {
    position: absolute;
    top: 32px;
    left: 505px;
    font-size: 96px;
}

.my-expertise {
    position: absolute;
    top: 212px;
    left: 151px;
    font-size: 40px;
    font-weight: 700;
    color: #fff;
}

.web-developmentfrontendbacke {
    position: absolute;
    top: 378px;
    left: 151px;
    font-weight: 700;
}

.web-design {
    position: absolute;
    top: 378px;
    left: 630px;
    font-weight: 700;
}

.uiux-design {
    position: absolute;
    top: 378px;
    left: 797px;
    font-weight: 700;
}

.i-specialise-in {
    position: absolute;
    top: 272px;
    left: 150px;
    font-size: 20px;
    font-weight: 300;
    color: #fff;
    text-align: left;
    display: flex;
    align-items: center;
    width: 784px;
}

.my-digital-toolbox {
    position: absolute;
    top: 488px;
    left: 150px;
    font-size: 40px;
    font-weight: 700;
    color: #fff;
}

.mongodb-icon-1 {
    position: absolute;
    top: 566px;
    left: 173px;
    width: 26.9px;
    height: 60px;
    object-fit: cover;
}

.django-icon-1 {
    position: absolute;
    top: 564px;
    left: 313px;
    width: 62px;
    height: 72px;
    object-fit: cover;
}

.vue-js-icon-1 {
    position: absolute;
    top: 571px;
    left: 226px;
    width: 68px;
    height: 58px;
    object-fit: cover;
}

.nuxt-js-icon-1 {
    position: absolute;
    top: 571px;
    left: 394px;
    width: 75px;
    height: 58px;
    object-fit: cover;
}

.tailwind-css-icon-1 {
    position: absolute;
    top: 571px;
    left: 495px;
    width: 81.9px;
    height: 50px;
    object-fit: cover;
}

.node-js-icon-1 {
    position: absolute;
    top: 571px;
    left: 613px;
    width: 51px;
    height: 58px;
    object-fit: cover;
}

.figma-icon-1 {
    position: absolute;
    top: 571px;
    left: 700px;
    width: 38.74px;
    height: 58px;
    object-fit: cover;
}

.service-section {
    position: relative;
    background-color: #000;
    width: 100%;
    height: 756px;
    overflow: hidden;
    text-align: center;
    font-size: 24px;
    color: rgba(255, 255, 255, 0.8);
    font-family: Inter;
}
</style>
