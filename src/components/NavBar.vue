<template>
  <div class="navbar">
    <div class="nav-links">
      <div class="about" href="#">About</div>
    <div class="services" href="#">Services</div>
    <div class="projects" href="#">Projects</div>
    <div class="button-open-links-navigate">Let's Talk</div>
    <img class="logo-tranwht-1-icon" alt="" src="../assets/logos/logo-tranWht.png" />

    </div>
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
    cursor: pointer;
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
    cursor: pointer;
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
    cursor: pointer;
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
    cursor: pointer;
    background-color: rgb(255, 255, 255);
    color: #000;
    border-radius: 5px;
    position: absolute;
    top: 5px;
    left: 954px;
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100px;
    height: 30px;
    font-size: 15px;

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
  
  .nav-link {
    cursor: pointer;
    display: none; /* Hide links by default for smaller screens */
  }


  .nav-links {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 10px; /* Add padding to create space between links */
  }
  @media screen and (min-width: 600px) {
    .nav-link {
      display: block; /* Show links for screens larger than 600px */
    }
  }
</style>
