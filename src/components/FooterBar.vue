<template>
    <div class="footer-section">
      <div class="basab-jha">
        <span class="span">©2023 </span>
        <span class="basab-jha1">BASAB JHA</span>
      </div>
      <div class="site-designed-and">Site designed and coded by basab w/ ❤️‍</div>
    </div>
  </template>
  <script>
    import { defineComponent } from "vue";
  
    export default defineComponent({
      name: "FooterSection",
    });
  </script>
  <style scoped>
    .span {
      font-weight: 300;
    }
    .basab-jha1 {
      font-weight: 800;
    }
    .basab-jha {
      position: absolute;
      top: 15px;
      left: 53px;
    }
    .site-designed-and {
      position: absolute;
      top: 15px;
      left: 568px;
      font-weight: 300;
    }
    .footer-section {
      position: relative;
      background-color: #000;
      width: 100%;
      height: 50px;
      text-align: center;
      font-size: 16px;
      color: #fff;
      font-family: Inter;
    }
  </style>
  