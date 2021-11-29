<template>
  <div id="app">
    <!-- <div class="header">
      <link rel="icon" type="image/png" sizes="32x32" href="./assets/images/favicon-32x32.png" />
       <p>Frontend Mentor | Article preview component</p>
    </div>-->
    <div class="body">
      <img src="./assets/images/drawers.jpg" alt />
      <div class="text">
        <span class="span1">{{ paragraph1 }}</span>
        <p>
          <span class="span2">{{ paragraph2 }}</span>
        </p>
        <div class="bottom ">
          <div class="bottom-left">
            <img src="./assets/images/avatar-michelle.jpg" alt />
            <div class="text-left">
              <p class="span5">{{ paragraph3 }}</p>
              <p>
                <span class="span6">{{ paragraph4 }}</span>
              </p>
            </div>
          </div>
          <div class="bottom-right">
            <div v-if="display">
          
              <div class="icones">
                <p class="share">Share</p>
                <img src="./assets/images/icon-facebook.svg" alt />
                <img src="./assets/images/icon-pinterest.svg" alt />
                <img src="./assets/images/icon-twitter.svg" alt />
              </div>
              <div class="traingle-code"></div>
            </div>
            <div>
              <img src="./assets/images/icon-share.svg" alt class="icone" @click="share" />
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="attribution">
      Challenge by
      <a
        href="https://www.frontendmentor.io?ref=challenge"
        target="_blank"
      >Frontend Mentor</a>.
      Coded by
      <a href="#">Your Name Here</a>.
    </div>
  </div>
</template>

<script>

export default {
  methods: {
    share() {
      this.display = !this.display;
    }
  },
  name: 'App',

  data() {
    return {
      display: false,
      paragraph1: "Shift the overall look and feel by adding these wonderful touches to furniture in your home",
      paragraph2: 'Ever been in a room and felt like something was missing? Perhapsit felt slightly bare and uninviting. I’ve got some simple tips         to help you make any room feel complete.',
      paragraph3: 'Michelle Appleton',
      paragraph4: '28 Jun 2020',
    }
  },
}
</script>

<style>
@import url("https://fonts.google.com/specimen/Manrope");
@import url("https://fontawesome.com");
@import url("https://icomoon.io");
@import url("https://ionicons.com");
.header {
  font-family: "Manrope";
  font-weight: 700;
}
.traingle-code {
  display: inline-block;
  height: 0;
  width: 0;
  border-top: 30px solid #8b8b8b;
  border-right: 17px solid transparent;
  border-left: 13px solid transparent;
  position: absolute;
  bottom: 290px;
  right: 210px;
}
.body {
  font-size: 13px;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  border: 1px solid #f3f3f3;
  border-radius: 25px;
  box-shadow: #000000 0px 5px 5px;
  overflow: hidden;
  margin: 10%;
}
.icones {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  align-items: center;
  background: #8b8b8b;
  width: 200px;
  position: absolute;
  border-radius: 15px;
  padding: 10px 0 10px 0;
  bottom: 320px;
  right: 125px;
}

.icone {
  width: 20px;
  height: 20px;
  background: #8b8b8b;
  border-radius: 50%;
  margin-top: 15px;
  padding: 5px;
  color: #f3f3f3;
}
.bottom {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  width: 100%;
}
.bottom-left {
  display: flex;
  justify-content: flex-start;
  align-items: center;
}
.bottom-left .span6 {
  font-size: 15px;
  color: #8c8c8c;
  padding-right: 25px;
}
.span5 {
  padding-top: 15px;
  font-size: 17px;
  font-weight: 700;
  color: #000;
}
.bottom-left img {
  margin-top: 15px;
  width: 50px;
  height: 50px;
  border-radius: 50%;
}
.text-left {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding-left: 10px;
}
.share {
  position: relative;
  font-size: 15px;
  font-weight: 500;
  color: #f3f3f3;
  /* padding-right: 25px;
  margin-top: 15px; */
}
.bottom-right {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  padding-right: 35px;
}
.text {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-left: 5%;
}
.text .span2 {
  font-weight: 500;
  font-size: 18px;
  color: #8c8c8c;
  font-size: 25px;
}
.text .span1 {
  font-size: 30px;
  font-weight: 700;
  color: #000;
  margin-top: 20px;
}
.attribution {
  font-size: 11px;
  text-align: center;
}
.attribution a {
  color: hsl(228, 45%, 44%);
}
@media screen and (max-width: 768px) {
  .body {
    display: flex;
    flex-direction: column;
  }
  .icones{
    position: static;
    width: 100%;
  }
  .traingle-code {
    display: none;
  }

}
</style>
