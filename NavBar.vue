<template>
  <div >
    <ul class="row ul2 father">
    <li><a class="li2 special" href="#">تنظیمات</a></li>
    <li><a class="li2" href="#">خرید اشتراک</a></li>
    <li><a class="li2" href="#">سبددانلود</a></li>
    <li><a class="li2" href="#">فیلم های مورد علاقه</a></li>
    <li><a class="li2" href="#">تیکت</a></li>
</ul>
  </div>
</template>

<script>

</script>

<style>
  @import "../assets/main.css";

  .ul2{
    background: transparent;
    margin-left: 0px;
    width: 100%;
}
.li2{
    background: transparent;
    border-bottom: 2px solid gray;
     padding: 10px 65px;
    font-size: 14px;
    font-family: Shabnam;
}
  .special{
    border-bottom: 2px solid black;
}
  .father{
    direction: rtl;

  }
  li {
    float: right;
    color: black;

}

li a {
    color: black;
    float: right;
    background: #ebebe0;
    text-align: center;
    padding: 14px 0px  ;
    text-decoration: none;
    font-size: 10px;
}

li a:hover {
    background-color: #e1e1e1;
}



ul {
    list-style-type: none;
    padding-right: 16%;
    text-align: center;
    overflow: hidden;
    background-color: #ebebe0;
}

</style>
