<template>
<div class="button_m " >
  <button class="btn1">{{this.title}}</button>
</div>
</template>
<script>
export default{
    props: ['title','back_color'],
  data:{
        activeColor: 'red',

  }

}
</script>
<style>
  @import "../assets/global.css";
  @import "https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-beta.2/css/bootstrap.min.css";

.button_m{
  color: white;
  border-radius: 7px;
  font-family: Shabnam;
  font-size: 12px;
  height: 40px;
  padding: 10px 10px;
  text-align: center;
  margin-top: 10px;
}
  .btn1{
    background-color: yellow;
    border: none;
    height: 30px;
    color: black;
    width: 100px;
    border: 2px solid white;
    border-radius: 12px;
  }

</style>
