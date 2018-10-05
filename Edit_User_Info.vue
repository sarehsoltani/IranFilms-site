<template>
  <div >

    <div class="container">
      <div class="row col-10 p-2" >
        <div class="col-md-8"></div>
        <div class="form-group col-md-10 col-sm-4 " style="margin-right: 270px">
        <div class="row col-3 pb-2 row1 w-50">  ویرایش اطلاعات کاربری</div>
        <div class="row  head1 mb-3 "></div>
        </div>
        <div class="col-3"></div>
        <div class="col-md-12 col-sm-12 sec1">
            <div class="form-group col-md-5 col-sm-6 w-50">
                   <div class=" title_class ">نام</div>
                   <input class=" head_con form-control input-sm "> </input>
            </div>

            <div class="form-group col-md-5 col-sm-6">
                   <div class=" title_class ">نام خانوادگی</div>
                   <input class=" head_con form-control input-sm "> </input>
            </div>

            <div class="form-group col-md-5 col-sm-6">
                   <div class=" title_class ">نام مستعار</div>
                   <input class=" head_con form-control input-sm "> </input>
            </div>

            <div class="form-group col-md-5 col-sm-6">
                   <div class=" title_class ">ایمیل(نام کاربری)</div>
                   <input class=" head_con form-control input-sm "> </input>
            </div>
        </div>

        <m_button class = "bg-success my_button " title="به روز رسانی"></m_button>

<!--<div class="title_class mr-5 pt-3 ">نام</div>-->
                <!--<input class="col-4 py-2 head_con mt-5 h-25 w-50 mr-0"> </input>-->

      </div>
    </div>
  </div>
</template>
<script>
  import header1 from '../components/header1.vue'
  import m_button from '../components/m_button.vue'
  import NavBar from '../components/NavBar.vue'
export default {
    components:{
      header1,
      m_button,
      NavBar,
    }
  }
</script>
<style scoped>
  @import '../assets/main.css';
  @import '../../node_modules/slick-carousel/slick/slick.css';
  @import '../assets/font/font-awesome-4.7.0/css/font-awesome.css';
  @import '../assets/font/font-awesome-4.7.0/css/font-awesome.min.css';
  @import '../assets/font/font-awesome-4.7.0/css/font-awesome.css';
  @import "https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css";
  @import "//maxcdn.bootstrapcdn.com/font-awesome/4.1.0/css/font-awesome.min.css";
  @import "https://fonts.googleapis.com/css?family=Roboto:300,400,500,700|Material+Icons";
  @import "https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-beta.2/css/bootstrap.min.css";

.sec1{
  margin-right: 240px;
}


  .head1{
    border-bottom: 1px solid lightgray;
    font-family: Shabnam;

}
  .row1{
    border-bottom: 2px solid #9c9c9c;
    color: #949494;
    font-family: Shabnam;
    font-weight: bold;


  }
  .head_con{
    border: 2px solid #d6d6d6;
    color: #949494;
    border-radius: 5px;
    background-color: #f4f4f4;
  }
  .my_button{
    width: 15%;
    margin-right: 270px;
    font-family: Shabnam;
    font-size: 14px;
  }
  .title_class{
    font-family: Shabnam;
    color: gray;
  }



</style>
