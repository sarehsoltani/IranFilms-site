<template>
  <div>
    <header1></header1>
    <search_back></search_back>
    <slider></slider>
    <static_banner class="mt-1" id="banner"></static_banner>
    <dynamic_slider id="hotslider"></dynamic_slider>
    <m_footer></m_footer>
  </div>



</template>

<script>
  import Slick from 'vue-slick'
  import static_banner from '../components/static_banner.vue'
  import slider from './slider.vue'
  import search_back from '../components/search_picture.vue'
  import header1 from '../components/header1.vue'
  import m_footer from '../components/m_footer.vue'
  import dynamic_slider from '../components/dynamic_slider.vue'

export default {
  data () {
    return {

    };
  },


   components: {
      Slick,
      static_banner,
      slider,
      header1,
     search_back,
      m_footer,
      dynamic_slider,
    },
  }
</script>

<style scoped>
  /*@import '../assets/main.css';*/
  @import '../../node_modules/slick-carousel/slick/slick.css';
  @import '../assets/font/font-awesome-4.7.0/css/font-awesome.css';
  @import '../assets/font/font-awesome-4.7.0/css/font-awesome.min.css';
  @import "https://fonts.googleapis.com/css?family=Roboto:300,400,500,700|Material+Icons";

  #banner{
    margin-top: -40vh;
  }


  #hotslider{
    background-color: white;
  }

  .sliderBar{
    background-color: black;
    width: 100%;
    height: 30px;
  }
</style>
