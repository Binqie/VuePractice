<template>
  <my-container>
    <div class="slider__wrapper">
      <div class="slider">
        <div class="slide" v-for="(item, idx) in 3" :key="idx">
          <img src="../../assets/slider/Bg.svg" alt="">
          <div class="slide__content">
            <div class="slide__badge">
              <img src="../../assets/slider/Badge.svg" alt="">
            </div>
            <div class="slide__recipes">
              <img src="../../assets/slider/Roll.svg" alt="">
              <span>Hot Recipes</span>
            </div>
            <div class="slide__info">
              <div class="slide__title">
                <h1>Spicy delicious chicken wings</h1>
              </div>
              <div class="slide__text">
                <span>Lorem ipsum dolor sit amet, consectetuipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqut enim ad minim</span>
              </div>
              <div class="slide__indicators">
                <div class="indicator time">
                  <img src="../../assets/slider/Timer.svg" alt="">
                  <span>30 Minutes</span>
                </div>
                <div class="indicator food">
                  <img src="../../assets/slider/ForkKnife.svg" alt="">
                  <span>Chicken</span>
                </div>
              </div>
            </div>
            <div class="slide__author">
              <div class="author">
                <div class="author__profile-photo">
                  <img src="../../assets/slider/User.svg" alt="">
                </div>
                <div class="author__info">
                  <div class="name">John Smith</div>
                  <div class="date">15 March 2022</div>
                </div>
              </div>
              <button class="view-recipes"><span>View Recipes</span></button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </my-container>
</template>

<script>

export default {
    name: 'my-slider',
}
</script>

<style>
.slider__wrapper {
  width: 1280px;
  height: 100%;
  width: auto;
  overflow: hidden;
}
.slider {
  width: 300%;
  position: relative;
  display: flex;
  flex-wrap: nowrap;
  justify-content: center;
}
.slide {
  width: 1280px;
  height: 100%;
  width: 100%;
  position: relative;
  margin: 0 20px;
}
.slide > img {
  width: 100%;
  height: 100%;
}
.slide__content {
  position: absolute;
  padding: 50px;
  top: 0;
  bottom: 0;
  left: 0;
  right: 50%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: flex-start;
}
.slide__badge {
  position: absolute;
  top: 50px;
  left: 100%;
  transform: translateX(-50%);
}
.slide__badge > img {
  width: 150px;
  height: 150px;
}
.slide__recipes {
  background: #FFFFFF;
  border-radius: 30px;
  padding: 10px 20px;
  display: flex;
  align-items: center;
}
.slide__recipes > span { 
  margin-left: 10px;
}
.slide__title, .slide__text, .slide__indicators {
  display: flex;
  justify-content: flex-start;
  text-align: left;
  margin-bottom: 10px;
}
.slide__title {
  max-width: 90%;
  font-size: 22px;
}
.indicator {
  background-color: rgba(0, 0, 0, 0.05);
  padding: 8px 16px;
  border-radius: 20px;
  margin-right: 10px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.slide__author {
  display: flex;
  width: 100%;
  align-items: center;
  justify-content: space-between;
}
.author {
  display: flex;
  align-items: center;
}
.author__info {
  margin-left: 10px;
}
.author__info > .name {
  font-size: 16px;
  font-weight: bold;
}
.view-recipes {
  font-size: 14px;
  padding: 22px 75px 22px 36px;
  border-radius: 15px;
  background: #000;
  color: #FFFFFF;
}
.view-recipes > span {
  position: relative;
}
.view-recipes > span::after {
  content: url('../../assets/slider/PlayCircle.svg');
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  margin-left: 10px;
}
</style>