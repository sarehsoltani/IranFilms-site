<template>
  <div>
    <div class="slide">
      <div class="1">
        <slick ref="slick"  class="slider-for"  :options="{slidesToShow: 1,slidesToScroll: 1,arrows: true,fade: false,prevArrow: false,nextArrow: false, asNavFor: '.slider-nav'}">
            <img v-for="item in SliderImages"  class="slider1" :src="item.image" >
        </slick>

        <div class="component">
            <q-toolbar class="header" color="primary" inverted>
              <div class="login">
                <router-link to="/login">
                  <q-btn id="ordinarybtn" small flat>ورود</q-btn>
                </router-link>
                <router-link to="/register">
                  <q-btn id="bluebtn"small flat>ثبت نام</q-btn>
                 </router-link>
              </div>
              <div class="logo">
                <i id="game" class="fa fa-gamepad" aria-hidden="true"></i>
                <span>امیرکبیر </span><a>استودیو</a>
              </div>
            </q-toolbar>
            <div class="trailer" >
              <q-btn class="gamebtn">ورود به صفحه ی بازی</q-btn>
              <div class="play">
                <i id="icon_trailer" class="fa fa-play-circle" aria-hidden="true"></i>
                <h id="icon_title">تریلر این بازی</h>
              </div>
            </div>
        </div>
      </div >
      <div class="2">
        <slick ref="slick" autoplay="true" class="slider-nav" :options="{slidesToShow: 3,slidesToScroll: 1,asNavFor: '.slider-for',dots: false,prevArrow: false, nextArrow: false,autoplaySpeed: 2000,autoplay: true, centerMode: true,focusOnSelect: true,pauseOnFocus: false}">
         <div class="SliderContainer" v-for="item in SliderImages">
          <img class="slider" :src="item.image" >
         </div>
        </slick>
      </div>
    </div>

  </div>
</template>

<script>
  import Slick from 'vue-slick'
  import axios from 'axios'
  import
  {
    QBtn,
    QIcon,
    QToolbar,
    QSearch,
    QCard,
    QCardMedia,

  } from 'quasar'

  export default {
    data () {
      return {
         SliderImages: [
          {
            image: '../statics/images/1.jpg'
          },
          {
            image: '../statics/images/2.jpg'
          },
          {
            image: '../statics/images/3.jpg'
          },
          {
            image: '../statics/images/4.jpg'
          },
          {
            image: '../statics/images/5.jpg'
          },
          {
            image: '../statics/images/6.jpg'
          },
          {
            image: '../statics/images/7.jpg'
          },

        ]
//        images: [require('../statics/images/1.jpg'), require('../statics/images/2.jpg'), require('../statics/images/3.jpg'), require('../statics/images/4.jpg'), require('../statics/images/5.jpg'), require('../statics/images/6.jpg') , require('../statics/images/7.jpg')],
      }
    },
    computed: {
    },
    methods: {
      async getGameList(){
        let list = await axios.get('http://api.ie.ce-it.ir/F95/home')
        console.log(list)
      }
    },
    created (){
      this.getGameList()
    },
    components: {
      Slick,
      QBtn,
      QIcon,
      QToolbar,
      QSearch,
      QCard,
      QCardMedia,
    },
  }
</script>

<style>
  @import '../../node_modules/slick-carousel/slick/slick.css';
   @import '../statics/fonts/font-face.css';
  @import '../statics/font-awesome-4.7.0/css/font-awesome.css';
  @import '../statics/font-awesome-4.7.0/css/font-awesome.min.css';

  .slider {
    width: 100%;
    height: 120px;
    margin-left: 0px;
    background-color: blue;
  }

 .slider1 {
   height: 70vh;
   margin-bottom: 1px;
 }
 .slider:hover{
   height: 150px;
   width: 170px;
   opacity: 0.1;

 }
 .SliderContainer{
   background-color: blue;
 }
.slide{
  display: flex;
  flex-direction: column;
}
.1 {
  position: relative;
  }
  .component {
    z-index: 1;
    position: absolute;
    top: 0;
    width: 100%;
  }

  .header {
    display: flex;
    align-items: center;
    flex-direction: row;
    justify-content: flex-start;
    font-family: 'shabnam';
    font-size: 12px;
  }
   .logo {
    display: flex;
    flex-direction: row-reverse;
    justify-content: flex-start;
    font-family: 'Shabnam';
    font-size: 10px;
     margin-right: 40px;
     width: 100%;
  }
   .login {
      width: 100%;
     display: flex;
     flex-direction: row-reverse;
     margin-right: 200px;
     font-size: 0.8em;
     font-family: 'shabnam';

   }
    #game {
    font-size: 1.6em;
    color: gray;
    padding-left: 2px;
  }
  span{
    color: white;
  }
  #bluebtn{
    background-color: blue;
  }

  .trailer {
    margin-top: 30vh;
    display: flex;
    flex-direction: row-reverse;
    justify-content: flex-start;
    font-family: 'shabnam';
    margin-right: 50px;
    width: 100%;

  }
  .gamebtn{
    background-color: blue;
    font-family: 'shabnam';
    font-size: 5px;
    /*height: 30px;*/
    margin-right: 100px;

    /*height: 2px;*/
  }

  .play {
    color: white;
    font-size: 12px;
    display: flex;
    flex-direction: row-reverse;
    width: 100%;
  }
  #icon_trailer{
    padding: 5px;
    margin-top: 10px;
  }
  #icon_title {
    margin-top: 10px;
    margin-right: 6px;
  }

</style>
