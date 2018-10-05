<template>

  <div class="cover1">
        <div class="sliderBar">
          <a href="#"> همه</a>
          <a href="#">فیلم سینمایی</a>
          <a href="#">انیمیشن</a>
          <a href="#">مستند</a>
          <a href="#">دوبله</a>
          <a href="#" id="lastitem">جدیدترین عناویــن</a>
        </div>
    <slick ref="slick" :options="slickOptions" class="slider1">
      <a href="#"><img class="img1" src="../assets/images/1.jpg" alt=""></a>
      <a href="#"><img class="img1" src="../assets/images/2.jpeg" alt=""></a>
      <a href="#"><img class="img1" src="../assets/images/3.jpg" alt=""></a>
      <a href="#"><img class="img1" src="../assets/images/4.jpg" alt=""></a>
      <a href="#"><img class="img1" src="../assets/images/5.jpg" alt=""></a>
      <a href="#"><img class="img1" src="../assets/images/6.jpg" alt=""></a>
      <a href="#"><img class="img1" src="../assets/images/7.jpg" alt=""></a>
      <a href="#"><img class="img1" src="../assets/images/8.jpg" alt=""></a>
      <a href="#"><img class="img1" src="../assets/images/9.jpg" alt=""></a>
      <a href="#"><img class="img1" src="../assets/images/10.jpg" alt=""></a>
      <a href="#"><img class="img1" src="../assets/images/11.jpg" alt=""></a>
      <a href="#"><img class="img1" src="../assets/images/12.jpg" alt=""></a>
      <a href="#"><img class="img1" src="../assets/images/5.jpg" alt=""></a>
      <a href="#"><img class="img1" src="../assets/images/9.jpg" alt=""></a>
      <a href="#"><img class="img1" src="../assets/images/4.jpg" alt=""></a>
    </slick>
  </div>


</template>

<script>
  import Slick from 'vue-slick'

  export default {
    components: {
      Slick,
    },
    props: {
      images: Array,
    },
    data () {
      return {

           slickOptions: {
        centerMode: true,
        arrows: true,
        centerPadding: '10px',
        slidesToShow: 4,

        responsive: [
          {
            breakpoint: 768,
            settings: {

              centerMode: true,

              centerPadding: '40px',
              slidesToShow: 3
            }
          },
          {
            breakpoint: 480,
            settings: {
              arrows: true,
              centerMode: true,
              centerPadding: '40px',
              slidesToShow: 1
            }
          }
        ]
      },
    };
  },
    methods: {

    }


  }
</script>

<style scoped>
  @import '../../node_modules/slick-carousel/slick/slick.css';
  @import '../assets/slick/slick.css';
  @import '../assets/slick/slick-theme.css';
  @import '../assets/main.css';

  .cover1{
    background-color: black;
    margin-left: -10px;
    margin-right: -10px;
    margin-bottom: -1vh;
    height: 50vh;
}
  .slider1{
    margin-right: 9vw;
    margin-left: 9vw;
   }
.img1{
  width: 250px;
    height: 270px;
    padding: 0px;
  margin-top: 2vh;
}
  .img1:hover{
    background-color: black;
  }
</style>


