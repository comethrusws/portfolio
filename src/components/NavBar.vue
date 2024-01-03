<template>
  <div class="navbar">
    <div class="about">About</div>
    <div class="services">Services</div>
    <div class="projects">Projects</div>
    <img class="logo-tranwht-1-icon" alt="" src="../assets/logos/logo-tranWht.png" />
    <div class="button-open-links-navigate" />
  </div>
</template>
<script>
  import { defineComponent } from "vue";

  export default defineComponent({
    name: "NavBar",
  });
</script>
<style scoped>
  .about {
    position: absolute;
    top: 22px;
    left: 535px;
    display: flex;
    align-items: center;
    justify-content: center;
    width: 72px;
    height: 1px;
  }
  .services {
    position: absolute;
    top: 22px;
    left: 656px;
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100px;
    height: 1px;
  }
  .projects {
    position: absolute;
    top: 22px;
    left: 805px;
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100px;
    height: 1px;
  }
  .logo-tranwht-1-icon {
    position: absolute;
    top: -5px;
    left: 280px;
    width: 50px;
    height: 50px;
    object-fit: cover;
  }
  .button-open-links-navigate {
    position: relative;
    width: 171px;
    height: 55px;
  }
  .navbar {
    position: relative;
    background: linear-gradient(rgba(0, 0, 0, 0.2), rgba(0, 0, 0, 0.2)), #000;
    width: 100%;
    height: 40px;
    overflow: hidden;
    text-align: center;
    font-size: 24px;
    color: #fff;
    font-family: Inter;
  }
</style>
