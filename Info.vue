<template>
  <div >
    <!--<header1></header1>-->
    <nav_bar></nav_bar>
    <div class="container tmp">
      <div class="row col-12 m-4 px-4 py-3">
        <div>
          <div class="child sp pt-4 pb-2">ویرایش اطلاعات کاربری</div>
          <div class="child pt-4 pb-2">تغییر رمز عبور</div>
          <div class="child pt-4 pb-2">انتقال اشتراک از سایت قدیم</div>
          <div class="child pt-4 pb-2">دعوت دوستان</div>
        </div>
        <div class="row mr-2">
            <div class="vl_1 mt-0 h-50 mh-50"></div>
            <div class="vl_2 mt-5 h-75 mh-50"></div>
        </div>
        <div class="row col-2 mr-5 pr-2 pb-2 pt-3 head_ch h-25">  شماره همراه</div>
        <div class="row col-8 head1 h-25 w-100"></div>
        <input class="row col-4 py-1 px-1 head_con w-50 ">
        <m_button class = "row bg-success my_button" title="ذخیره شماره تماس"></m_button>
      </div>
      <div class="row">
         <Edit_User_Info></Edit_User_Info>
      </div>


    </div>
  </div>
</template>
<script>
  import header1 from '../components/header1.vue'
  import m_button from '../components/m_button.vue'
  import nav_bar from '../components/NavBar.vue'
  import Edit_User_Info from '../components/Edit_User_Info.vue'

export default {
    components:{
      header1,
      m_button,
      nav_bar,
      Edit_User_Info
    }
  }
</script>

<style scoped>
  @import '../assets/font/font-awesome-4.7.0/css/font-awesome.css';
  @import '../assets/font/font-awesome-4.7.0/css/font-awesome.min.css';
  @import "https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-beta.2/css/bootstrap.min.css";
  /*@import "../assets/main.css";*/
  .child{
    /*padding: 12px;*/
    font-family: Shabnam;
  }
  .sp{
    color: blue;
  }
  .div2{
  }

  .vl_1 {
    border-left: 6px solid blue;
    border-radius: 20%;
    height: 50px;
    position: relative;
}
   .vl_2 {
    border-left: 6px solid gray;
    border-radius: 15%;
    height: 50px;
     position: absolute;
     /*margin-top: 100px;*/
}
  .head1{
    border-bottom: 1px solid lightgray;
    position: absolute;
    top : 0;
    margin-right: 230px;

}
  .head_ch{
    border-bottom: 2px solid #9c9c9c;
    color: #949494;
    font-family: Shabnam;
    font-weight: bold;
  }
  .head_con{
    border: 2px solid #d6d6d6;
    color: #949494;
    position: absolute;
    margin-right: 220px;
    /*width: 60% ;*/
    border-radius: 5px;
    margin-top: 80px;
    background-color: #f4f4f4;
  }
  .my_button{
    /*width: 15%;*/
    margin-top: 170px;
    position: absolute;
    margin-right: 220px;
    font-family: Shabnam;
    font-weight: bold;
    font-size: 12px;
  }
  .tmp{
    direction: rtl;
  }


</style>
