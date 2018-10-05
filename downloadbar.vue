<template>
 <div class="container">
   <ul class="mov_menu">
     <li id="selected" ><a href="#" >دانلود</a></li>
     <li id="subtitle" ><a href="#" >زیرنویس</a></li>
     <li id="comment"  ><a href="#" >نظر کاربران</a></li>
     <li id="clar">   <a href="#" >نقد و بررسی</a></li>
     <li id="producer"><a href="#" >عوامل فیلم</a></li>
     <li id="awards" >  <a href="#" >جوایز</a></li>
     <li id="gallery" > <a href="#" >گالری</a></li>
   </ul>
 </div>
</template>

<script>
export default {

}
</script>

<style>
  @import "../assets/global.css";
  @import "../assets/main.css";
  @import '../assets/font/font-awesome-4.7.0/css/font-awesome.css';
  @import '../assets/font/font-awesome-4.7.0/css/font-awesome.min.css';
  @import "https://fonts.googleapis.com/css?family=Roboto:300,400,500,700|Material+Icons";

  .container{
    /*margin-right: 17vw;*/
    font-family: Shabnam;
}

.mov_menu{
    display: flex;
    flex-direction: row-reverse;
  margin-right: -1vw;
  margin-left: -1vw;
    /*justify-content: flex-start;*/
}

.container ul {
    padding: 0;
    list-style: none;
    /*width: 100%;*/
}
.container ul li {
    cursor: pointer;
    width: 300px;
}

.container ul li a {
    color: grey;
    font-size: 15px;
    font-weight: bold;
    text-align: center;
    line-height: 58px;
    padding: 0 20px;
    width: 100%;
    display: block;
    border-bottom: 3px solid #bbb;
    text-decoration: none;
}
.container ul li a:hover{
    border-bottom: 3px solid black;
}
.container ul li a:active{
     border-bottom: 3px solid black;
}

</style>
