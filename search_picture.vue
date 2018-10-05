<template>

        <div  class="picture_back">
            <div class="container col-12 search3 mr-3" style="padding-top:6%">
                <circle_button class="mx-2"></circle_button>
                <div class="search1">
                    <search_bar class="s1" ></search_bar>
                    <search_contain ></search_contain>
                </div>

            </div>
        </div>

</template>
<script>

    import search_bar from '../components/search_bar'
    import search_contain from '../components/search_contain'

    import circle_button from '../components/circle_button.vue'

    export default {
        components:{
            search_bar,
            search_contain,
            circle_button,

        }}
</script>
<style scoped>
    @import "https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-beta.2/css/bootstrap.min.css";

    .picture_back{
        padding-top:10%;
        background-image: url("../assets/images/2.jpeg");
        height:100vh;
        background-position: center;
        background-repeat: no-repeat;
        background-color: black;
        background-size: contain;

background-position: center;


    }

    .search1{
        z-index: 10;
        direction:ltr;
           }

    .s1{
        overflow: hidden;
    }
    .slider1{
        padding: 2px;
    }

    .search3{
      display: flex;
      flex-direction: row-reverse;
      justify-content: center;
    }

</style>
