<template>
    <div class="circle mt-5">
        <div class="button_circle ic1 ">
            <i class="fa fa-search-plus fa-2x ico1" aria-hidden="true"></i>
        </div>
        <div class="button_circle ic2 ">
            <i class="fa fa-search fa-2x ico" aria-hidden="true"></i>
        </div>
    </div>
</template>
<script>

</script>
<style>
  @import "../assets/global.css";
  @import '../assets/font/font-awesome-4.7.0/css/font-awesome.css';
  @import '../assets/font/font-awesome-4.7.0/css/font-awesome.min.css';
  @import "https://fonts.googleapis.com/css?family=Roboto:300,400,500,700|Material+Icons";
  @import "https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-beta.2/css/bootstrap.min.css";
    .button_circle{
        position: relative;
        background-color: #ffa922;
        border-radius: 50%;
        color: white;
        width:44px;
        height:44px;
    }
    .ico1{
        position: absolute;
        top:10px;
        right: 10px;
    }
    .ico{
        position: absolute;
        top:10px;
        right:10px;
    }

    .ic1{
        background-color: #b625d0;
    }
    .ic2{
        background-color: #05c371;
    }

    .circle{
     display: flex;
      flex-direction: row-reverse;
    }
</style>
