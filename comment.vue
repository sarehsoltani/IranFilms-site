<template>
   <div class="container outer p-4 mr-6 ">
        <div class="row  pl-3 pt-3 d-flex pr-3  justify-content-between">
            <div class="rating">
                <div class="mt-4"><M_Slider  title="کارگردانی" @updatep="updateDirector"></M_Slider></div>
                <div class="mt-4"><M_Slider  title="بازیگری" @updatep="updateAct"></M_Slider></div>
                <div class="mt-4"><M_Slider  title="فیلم نامه" @updatep="updateScr"></M_Slider></div>
            </div>

            <div class="voter col-2  mr-4">
                <img src="../assets/images/sare.jpg">
            </div>
            <div class="comment col-5">
                <!--<textarea  style="overflow:hidden" class="row-4 comment_txt col-4 mt-3" >oooo-->
              <vue-emoji @input="onInput2"  width="400" height="100" class="comment_txt mt-2"></vue-emoji>

                <div class="choiceidea">
                    <input type="radio" name="idea" value="0"> نظری ندارم
                    <input type="radio" name="idea" value="1" checked>پیشنهاد نمی کنم
                    <input type="radio" name="idea" value="2" checked>پیشنهاد می کنم
                </div>
            </div>
        </div>

       <div class="row mt-3">
           <button id="comment_btn" @click="sendCm" type="submit">ثبت دیدگاه</button>
       </div>

        </div>


</template>

<script>
    import M_Slider from '../components/M_Slider.vue'
    import VueEmoji from 'emoji-vue'
   export default {
        props:['text'],
        data(){
            return {
                id:1,
                msg2: '',
                rates:{
                    director:'',
                    act:'',
                    scr:'',
                },
            }
        },
        methods: {

            onInput2(event) {
                this.msg2 = event.data;
            },
            sendCm(){
                var data ={
                    author:'sare', comment:this.msg2, rate_director:this.rates.director,
                    rate_actor:this.rates.act,
                    rate_film:this.rates.scr,
                }
                window.axios.post(`/movies/${this.id}/comments`, data).then(function (result) {
                    console.log(_this.result)
                })
            },
            updateDirector(data){
                this.rates.director = data.value / 2
            },
            updateAct(data){
                this.rates.act = data.value / 2
            },
            updateScr(data){
                this.rates.scr = data.value / 2
            },
        },
        components: {
            M_Slider,
            VueEmoji
        }
    }


</script>


<style scoped>
    @import "https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-beta.2/css/bootstrap.min.css";
    @import "../assets/main.css";

    .rating{
      font-weight: bold;
      font-family: Shabnam;
    }
  .comment_txt{
    font-family: Shabnam;
    font-size: 15px;
    border: none;
    font-weight: bold;
    text-align: right;
  }

  .choiceidea{
    font-family: Shabnam;
    margin-top: 6vh;
  }

  .outer{
    border: solid;
    border-bottom-right-radius:10px;
    border-bottom-left-radius: 10px;
    border-top: none;
    margin-top: -5vh;
    border-color: #ededed;
    direction: rtl;
}



.comment{
    border:solid;
    border-radius: 10px;
    border-color: #ededed;
    font-family: Shabnam;

}



.voter{
    display: inline-flex;
    align-items: center;
}
.voter img{
    width: 120px;
    height: 120px;
    border-radius: 50%;
    border: none;
}



#comment_btn{
    font-family: Shabnam;
    color: white;
    background-color: #00cc99;
    border: none;
    border-radius: 10px;
    padding: 8px;
    width: 100px;
    margin-top: 10px;
    margin-right: 152vh;

}
#comment_btn:hover{
    background-color: darkblue;
    cursor: pointer;
}

  .choiceidea input{
    margin-right: 10px;
    padding: 20px;
  }


</style>
