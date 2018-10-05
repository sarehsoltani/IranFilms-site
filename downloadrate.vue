<template>
  <div>
    <div class="comment">
      <div class="rating">
        <label class="rate"> ارزش دانلود ۸ از ۱۰</label>
        <div class="d-flex row mt-2 mr-1">
          <div class="track1 h-25 w-25"></div>
          <div class="track2 h-25 w-50"></div>
        </div>
        <p>نتایج آرا کاربران بر اساس کارگردانی + بازیگری + فیلمنامه</p>
      </div>
      <div class="commenttxt">
        <p>۶۴  نفر از ۷۲ نفر تماشای این فیلم را
          <br>                 پیشنهاد کردند
        </p>
      </div>
      <div class="message">
        <p>شما هم براساس ارزش دانلود به فیلم
          <br>رای دهید.</p>
        <a class="btn">امتیاز دهید</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
  @import "../assets/global.css";
  /*@import "../assets/main.css";*/
   @import "https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-beta.2/css/bootstrap.min.css";
  @import '../assets/font/font-awesome-4.7.0/css/font-awesome.css';
  @import '../assets/font/font-awesome-4.7.0/css/font-awesome.min.css';

  .comment{
    display: flex;
    flex-direction: row-reverse;
    margin-right: 16vw;
    margin-left: 10vw;
    justify-content: flex-start;
    font-family: Shabnam;
    margin-bottom:3vh ;
    margin-top: 12vh;
}

 .rating{
    display: flex;
    flex-direction: column;
   justify-content: flex-start;
}

.rate{
    color: #15c578;
    font-family: Shabnam;
    font-size: 15px;
    font-weight: bold;
    margin-bottom: 1vh;
    text-align: right;
    border: none;
}



.rating p{
    text-align: right;
    font-weight: bold;
    color: #b3b3b3;
    margin-top: 2vh;
}

.commenttxt p{
    color: blue;
    font-weight: bold;
    font-size: 15px;
    text-align: center;
    margin-right: 5vw;
    margin-top: 5vh;
    direction: rtl;
}

.message p{
    color: #b3b3b3;
    font-weight: bold;
    font-size: 14px;
    margin-right: 5vw;
    text-align: center;
    direction: rtl;
}
.message .btn{
    background: #3a6ee8;
    font-family: Shabnam;
    color: #fff;
    border-radius: 9px;
    height: 5vh ;
    margin-right: 11vh;
    font-size: 14px ;
    font-weight: 400;
    border: 1px solid transparent;
    text-decoration: none;
    text-align: justify;
}
  .track1{
    border: 3px solid #04B45F ;
    background-color: #04B45F;
    margin-left: -1vw;
}
.track2{

    border: 3px solid gray ;
    background-color: gray;
}
</style>
