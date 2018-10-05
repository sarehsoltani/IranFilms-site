<template>
  <div class="slider_class">
    <slick ref="slick" :options="slickOptions" class="slide_child">
      <div class="sh-carousel"  v-for="image in images" @mouseover="seen=true" @mouseout="seen=false">
            <div v-if="seen"  class="slider_cover  text-center"  >
                <div class="text-warning d-block">دانلود فیلم </div>
                <div class="">The Game</div>
                <div>2017</div>
                <div class="sh-carousel_icons d-flex justify-content-around">
                    <a href="#"><i class="fa fa-download"></i></a>
                    <a href="#"><i class="fa fa-thumbs-up"></i></a>
                    <a href="#"><i class="fa fa-play"></i></a>
                </div>
                <div class="">بازی</div>
            </div>
        <div class="w-50 h-50" >

        <div class="m-1"  >
      <div  class="img_slide px-2 " >

        <img class="picA w-75 h-75 container" :src="image.url" >
      </img>


         <div class="pt-1 mx-4 d-flex justify-content-between">
        <span class=" sp1 px-1 py-1 mr-1 text-center">جنایی</span>
        <span class="sp1  px-1 py-1 mr-1 text-center">راز</span>
        <span class=" sp1  px-1 py-1 text-center">هیجانی</span>
      </div>
      <div class="pt-1 d-flex  mx-4 justify-content-between">
        <span class="sp2 px-2 py-1 mr-2 text-center">BlueRay</span>
        <span class="sp2 px-2 py-1 text-center">
           7.0
          <i class="fa fa-star text-warning ml-1" aria-hidden="true"></i>
         </span>
      </div>
        </div>
        </div>
        </div>
      </div>
    </slick>
  </div>


</template>

<script>
  import Slick from 'vue-slick'

  export default {
      props:[],
    components: {
      Slick,
    },
    data () {
      return {
        slickOptions: {
          infinite: true,
          speed: 300,
          slidesToScroll: 4,
           slidesToShow: 5,
        },
        seen: false,
           images:[

            {
                url: '/static/images/3.jpg'
            },
            {
                url: '/static/images/4.jpg'
            },
             {
                url: '/static/images/5.jpg'
            },
             {
                url: '/static/images/5.jpg'
            },
            {
                url: '/static/images/7.jpg'
            },
            {
                url: '/static/images/6.jpg'
            },
            {
                url: '/static/images/7.jpg'
            },
            {
                url: '/static/images/8.jpg'
            },
            {
                url: '/static/images/11.jpg'
            },

          ]
      }
    },

  }
</script>

<style>
  @import '../../node_modules/slick-carousel/slick/slick.css';
  @import '../assets/slick/slick.css';
  @import '../assets/slick/slick-theme.css';
  @import "https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-beta.2/css/bootstrap.min.css";

  .slider_class{
    background-color: black;
    /*height: 45vh;*/
}
  .slide_child{
    margin-right: 9vw;
    margin-left: 9vw;
   }
  .slide_chid img :hover{
    background-color: black;
    cursor: pointer;
  }

  /*.img_slide{*/
    /*width: 200px;*/
    /*height: 200px;*/
    /*padding: 10px;*/
    /*margin-top: 2vh;*/
    /*background: linear-gradient(to top, maroon 50%, gray 50%);*/
  /*}*/

    .crauler{
    background-color: transparent;
    direction: ltr;
}

.crauler img{
    margin-left: 2%;
    width: 95%;
    height:240px;

}
.crauler div:first-child{
    color: white;
    font-size: 16px;
    direction: rtl!important;

}

.crauler div div button:first-child{
    padding: 0px 10px 0px 10px;
    border-radius: 5px;
    border:solid;
    background-color: gray;
}

.crauler .row button{
    margin-left: 5px;
    border:none;
    color: white;
    background-color: transparent;
    cursor: pointer;
}

.sh-carousel{
    position: relative;
}
.slider_cover{
    display: flex;
    flex-direction: column;
    justify-content: center;
    position: absolute;
    height: 100%;
    margin-top: 2vh;
    width: 95%;
    background-color: black;
}




.sh-carousel_icons a{
    text-decoration: none;
    color: white;
    font-size: 15px;
    display: flex;
    justify-content: center;
    align-items: center;
    border: 1px solid white;
    width: 40px;
    height: 40px;

    border-radius: 50%;

    transition: all 0.3s ease-out;
}
.sh-carousel_icons a:hover{
    color: black;
    background-color: white;
}

    .slider_class{
    background-color: black;
    /*height: 45vh;*/
}
  .slide_child{
    margin-right: 9vw;
    margin-left: 9vw;
   }
  .slide_chid img :hover{
    background-color: black;
    cursor: pointer;
  }

  .img_slide{
    width: 16Vw;
    height: 23vw;
    padding: 10px;
    margin-top: 2vh;
     background: linear-gradient(to top, #13578b 30%, gray 70%);
  }
  .picA{
      /*background-image: url('../assets/img/f1.jpg') ;*/
     /*background-size: cover;*/
  }

  .sp1{
    border: 4px solid #8e8e8e;
    background-color: #c1c1c1;
    border-radius: 8%;
    width: 120px;

  }
  .sp2{
    border: 2px solid #020202;
    background-color: transparent;
    border-radius: 10px;
    color: black;
    width: 200px;
  }

</style>
