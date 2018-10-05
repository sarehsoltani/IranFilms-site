<template>
  <div >
    <div  class="picture_back">
      <div class="search2 ">
        <circle_button></circle_button>
      </div>
      <div class="search1">
    <search_container class="s1" ></search_container>
    <search_input ></search_input>
        <m_button ></m_button>
    </div>
    </div>
  </div>
</template>
<script>

  import search_container from '../components/search_container.vue'
  import search_input from '../components/search_input.vue'
  import m_button from '../components/m_button.vue'
  import circle_button from '../components/circle_button.vue'

export default {
    components:{
      search_container,
      search_input,
      m_button,
      circle_button,

    }}
</script>
<style scoped>
  @import  url('../assets/awesomedoc/css/font-awesome.min.css');
.picture_back{
  background-image: url("../assets/img/s1.jpg");
  position:relative ;
  height: 400px;;
  background-position: center;
  background-repeat: no-repeat;
    background-size: cover;
}
  .father1{
    /*overflow: hidden;*/
  }
  .search2{
    margin-top: 140px;
    float: right;
    margin-right: 415px;
  }
  .search1{
    z-index: 10;
    width: 29%;
    padding: 100px 0px;
    float: left;
    margin-left: 550px;
  }
  .c1{
    float: right;

  }
  .s1{
    overflow: hidden;
  }
  .slider1{
    padding: 2px;
  }

</style>
