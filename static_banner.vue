<template>
  <div id="banner" class="row d-flex h-75">
    <img src='../assets/images/banner.png' class=" col-7  mt-4"/>
    <div id="inner_banner" class="col-3 mt-5 pt-3">
      <div id="p1" class="row-4 ">{{ message }}</div>
      <div id="p2" class="row-4 my-3">{{ message1 }}</div>
        <button id="downbtn" class=" mt-2 w-50 h-25 ml-5" >! به نجات زمین برین </button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: '!زندگی بشر رو به پایان است' ,
      message1: 'همه، خود را برای بقا آماده می کنند',
      active: false,
    };
    },
     methods: {
        mouseOver: function(){
        this.active = !this.active;
        }
    }

}
</script>

<style scoped>
  @import "https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-beta.2/css/bootstrap.min.css";
  @import "../assets/global.css";
#banner {
  background-color: black;
  background-size: cover;
}

#inner_banner{
  color: #cf4040;
  font-family: Shabnam;
}

#p1 {
  font-size: 1.7em;
}
#p2{
 font-size:1.2em;
}

#downbtn{
  background: transparent;
  font-family: Shabnam;
  font-weight: bold;
  border: 2px solid #cf4040;
  color: #cf4040;
  text-align: center;
  border-radius: 10px;

}

a{
  text-decoration: none;
}

#downbtn:hover{
  cursor: pointer;
  background-color: #cf4040;
  color: black;
}
</style>
