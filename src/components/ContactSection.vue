<template>
<div class="contact-section">
    <b class="contact">contact.</b>
    <img class="contact-section-child" alt="" src="../assets/texture/line4.png" />
    <img class="logo-blk-1-icon" alt="" src="../assets/logos/logo-blk.jpg" />
    <div class="contact-details">Contact Details</div>
    <a class="hellobasabjhacomnp" href="mailto:hello@basabjha.com.np" target="_blank" onclick="sendEmail()">hello@basabjha.com.np</a>
    <div class="my-digital-spaces">My Digital Spaces</div>
    <div class="bento"><a href="https://bento.me/basab">Bento</a></div>
    <div class="github"><a href="https://github.com/comethrusws">GitHub</a></div>
    <div class="linkedin"><a href="https://linkedin.com/in/basabjha">LinkedIn</a></div>
    <div class="youtube">YouTube</div>
    <div class="location">Location📍</div>
    <i class="kathmandu-nepal">Kathmandu, Nepal</i>
    <i class="pm">{{ currentTime }}</i>
    
    <i class="have-an-awesome">Have an awesome idea? Let's bring it to life.</i>

    <div class="contact-section-item" />
    <i class="your-name">Your Name</i>
    <div class="contact-section-inner" />
    <i class="your-email">Your Email</i>
    <div class="line-div" />
    <i class="your-message">Your Message</i>

    <button class="send-button"> Send Message.</button>

</div>
</template>

  
<script>
import {
    defineComponent
} from "vue";

export default defineComponent({
    name: "ContactSection",
    data() {
        return {
            currentTime: this.getCurrentTime()
        };
    },
    mounted() {
        setInterval(() => {
            this.currentTime = this.getCurrentTime();
        }, 1000);
    },
    methods: {
    getCurrentTime() {
      const kathmanduOffset = 5.75; // Nepal Timezone Offset (UTC+5:45)
      const now = new Date();
      const utc = now.getTime() + (now.getTimezoneOffset() * 60000);
      const kathmanduTime = new Date(utc + (3600000 * kathmanduOffset));
      const hours = kathmanduTime.getHours();
      const period = hours >= 12 ? 'PM' : 'AM';
      const formattedHours = hours % 12 || 12; // Convert hours to 12-hour format
      const minutes = kathmanduTime.getMinutes();
      const seconds = kathmanduTime.getSeconds();
      return `${this.formatTime(formattedHours)}:${this.formatTime(minutes)}:${this.formatTime(seconds)} ${period}`;
    },
    formatTime(time) {
      return time < 10 ? `0${time}` : time;
    },
    sendEmail() {
      const recipient = 'hello@basabjha.com.np';
      const subject = 'Subject of the email';
      const body = 'Content of the email.';

      const mailtoLink = `mailto:${recipient}?subject=${encodeURIComponent(subject)}&body=${encodeURIComponent(body)}`;

      window.location.href = mailtoLink;
    }
  }
});
</script>
  
<style scoped>
.contact {
    position: absolute;
    top: 44px;
    left: 524px;
    font-size: 96px;
    text-align: center;
}

.contact-section-child {
    position: absolute;
    top: 162px;
    left: 490.99px;
    max-height: 100%;
    width: 450px;
    object-fit: cover;
}

.logo-blk-1-icon {
    position: absolute;
    top: 52px;
    left: 1250px;
    border-radius: 100px;
    width: 80px;
    height: 80px;
    object-fit: cover;
}

a{
    text-decoration: none;
    cursor: pointer;
    color: #000;
}
.contact-details {
    position: absolute;
    top: 256px;
    left: 1033px;
    font-size: 32px;
    font-weight: 600;
    text-align: center;
}

.hellobasabjhacomnp {
    position: absolute;
    top: 300px;
    left: 1033px;
    text-decoration: none;
    font-style: italic;
    font-weight: 300;
    color: #000;
    text-align: center;
}

.my-digital-spaces {
    position: absolute;
    top: 414px;
    left: 1033px;
    font-size: 32px;
    font-weight: 600;
    text-align: center;
}

.bento {
    position: absolute;
    top: 470px;
    left: 1033px;
    font-weight: 500;
    color: #000;
}

.github {
    position: absolute;
    top: 562px;
    left: 1033px;
    font-weight: 500;
    color: #000;
}

.linkedin {
    position: absolute;
    top: 516px;
    left: 1033px;
    font-weight: 500;
    color: #000;
}

.youtube {
    cursor: pointer;
    position: absolute;
    top: 608px;
    left: 1033px;
    font-weight: 500;
    color: #000;
}

.location {
    position: absolute;
    top: 700px;
    left: 1033px;
    font-size: 32px;
    font-weight: 600;
}

.kathmandu-nepal {
    position: absolute;
    top: 744px;
    left: 1033px;
    font-weight: 300;
    color: #000;
}

.pm {
    position: absolute;
    top: 778px;
    left: 1033px;
    font-weight: 300;
    color: #000;
}

.have-an-awesome {
    position: absolute;
    top: 256px;
    left: 134px;
    font-size: 40px;
    display: flex;
    font-weight: 600;
    align-items: center;
    width: 476px;
    height: 88px;
}

.contact-section-item {
    position: absolute;
    top: 444.5px;
    left: 133.5px;
    border-top: 1px solid rgba(0, 0, 0, 0.8);
    box-sizing: border-box;
    width: 281px;
    height: 1px;
}

.your-name {
    position: absolute;
    top: 419px;
    left: 134px;
    font-size: 16px;
    font-weight: 300;
}

.contact-section-inner {
    position: absolute;
    top: 444.5px;
    left: 490.5px;
    border-top: 1px solid rgba(0, 0, 0, 0.8);
    box-sizing: border-box;
    width: 281px;
    height: 1px;
}

.your-email {
    position: absolute;
    top: 419px;
    left: 491px;
    font-size: 16px;
    font-weight: 300;
}

.line-div {
    position: absolute;
    top: 607.5px;
    left: 133.5px;
    border-top: 1px solid rgba(0, 0, 0, 0.8);
    box-sizing: border-box;
    width: 638px;
    height: 1px;
}

.your-message {
    position: absolute;
    top: 583px;
    left: 134px;
    font-size: 16px;
    font-weight: 300;
}

.send-button {
    cursor: pointer;
    outline: none;
    z-index: -1;
    position: absolute;
    top: 651px;
    left: 134px;
    border-radius: 40px;
    background-color: rgb(5, 5, 5);
    width: 200px;
    height: 40px;
    font-size: 16px;
    font-weight: 300;
    color: #fff;
}

.contact-section {
    position: relative;
    background-color: rgba(255, 255, 255, 0.8);
    width: 100%;
    height: 940px;
    overflow: hidden;
    text-align: left;
    font-size: 24px;
    color: rgba(0, 0, 0, 0.8);
    font-family: Inter;
}
</style>
