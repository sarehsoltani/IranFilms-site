<template>
  <div>
    <slider></slider>
    <!--<div class="poster">-->
      <!--<img id="img2" src="../assets/images/1.jpg"/>-->
      <!--<div class="TypeOfFilm">-->
        <!--<label id="Type1" class="type">کمدی</label>-->
        <!--<label class="type">درام</label>-->
        <!--<label id="Type2" class="type">جنایی</label>-->
      <!--</div>-->
    <!--</div>-->

  </div>

</template>

<script>
  import  slider from './slider.vue'
export default {
  components:{
     slider,
    }
}
</script>

<style>
    @import '../assets/main.css';
    @import "https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-beta.2/css/bootstrap.min.css";
  .poster{
    width: 200px;
    height: 300px;
    margin: auto;
    background: linear-gradient(to top, maroon 30%, gray 70%);
    display: flex;
    flex-direction: column-reverse;
  }

  #sec1{
    width: 200px;
    margin: auto;
    height: 130px;
    background-color: gray;
  }
   #sec2{
    margin: auto;
    width: 200px;
    height: 170px;
    background-color:blueviolet ;
  }

  #img1{
    width: 130px;
    height: 150px;
    margin-top: -17vh;
    position: absolute;
  }
  #img1:hover{
    background-color: black;
  }
body{
    overflow-y:hidden;
}
  /*.poster_Info{*/
    /*display: flex;*/
    /*padding-left: 2.5vw;*/
    /*margin-bottom: -20vh;*/
    /*flex-direction: column;*/
    /*margin: auto;*/
  /*}*/

  /*.TypeFilms{*/
    /*display: flex;*/
    /*flex-direction: row-reverse;*/
    /*margin-bottom: 2vh*/
  /*}*/
  .type{
    background-color: whitesmoke;
    width: 20px;
    height: 2vh;
    padding: 1vh;
    /*margin-right: 1vw;*/
    /*margin-left: 1vw;*/
    margin-bottom: 11vh;
    font-family: Shabnam;
    font-size: 10px;
    border: 2px solid black;
  }
  #img2{
    width: 150px;
    height: 180px;
    position: absolute;
    margin: auto;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    margin-bottom: 61vh;
  }

  .TypeOfFilm{
    display: flex;
    flex-direction: row-reverse;
    align-items: center;
    margin-left: 30vw;
    margin-right: 50vw;

    /*justify-content: space-between;*/
    /*position: absolute;*/
  }

  #Type1{
    /*margin-right: 2vw;*/
  }

  #Type2{
    /*margin-left: -5vw;*/
  }
</style>
