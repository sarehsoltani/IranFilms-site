<template>
  <div class="movie_detail ">
        <div class="FilmPath">
            <a href="#">خانه</a>
            <i class="fa fa-chevron-left" aria-hidden="true"></i>
            <a href="#">فیلم</a>
            <i class="fa fa-chevron-left" aria-hidden="true"></i>
            <a  href="#">  دانلود فیلم {{MovieTitle}}  </a>
        </div>
        <div class="FilmInfo">
            <div class="Title">
                <a id="name" href="#"> {{MovieTitle}}دانلود فیلم </a>
            </div>
            <div class="MovieType">
                <button id="btn1">کمدی</button>
                <button id="btn2">درام</button>
                <button id="btn3">جنایی</button>
            </div>
            <div class="headercontent">
                <div class="infoGradient bottomGradient"></div>
                <div class="infoGradient"></div>
            </div>
            <div id="MovieImg"><img id="film" src="../assets/images/sare.jpg"></div>
            <div class="detail">
                <div class="Info1">
                    <div id="Score"><i class="fa fa-star" aria-hidden="true"></i>{{rate}}</div>
                    <div id="imdb">IMDB</div>
                    <div id="subscene">Subscene</div>
                </div>
                <div class="Info2">
                    <a id="year">{{year}}</a>
                    <a id="length">{{length}}</a>
                    <a id="language">ٍEnglish</a>
                    <a id="gp">G</a>
                    <a id="country"> {{country}} </a>
                </div>
                <div class="divisionline"></div>
                <div id="description">{{description}}</div>
                <div class="divisionline1"></div>
                <div class="Info3">
                    <div id="director"> director: {{director}} </div>
                    <div id="author">authors :{{authors}}</div>
                    <div id="stars">stars: {{stars}} </div>
                </div>
            </div>

        </div>



  </div>
</template>

<script>
export default {
  props:['MovieTitle','rate','year','length','language','director','description','country','authors','stars'],
}
</script>

<style scoped>
  @import "../assets/movie_detail.css";
  @import "../assets/global.css";
  @import "../assets/main.css";
  @import '../assets/font/font-awesome-4.7.0/css/font-awesome.css';
  @import '../assets/font/font-awesome-4.7.0/css/font-awesome.min.css';
  @import "https://fonts.googleapis.com/css?family=Roboto:300,400,500,700|Material+Icons";

.Info3{
  font-size:15px;
  /*direction: rtl;*/
  margin-right: -5vw;
}

</style>
