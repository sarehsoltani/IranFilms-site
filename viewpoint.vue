<template>
    <div class="container mb-5 mt-5">
        <div class="comment p-5 d-flex" :class="{agree : status ==1 , disagree : status ==2}">
            <span class="star" v-if="status==1">
                <i class="fa fa-star-o" aria-hidden="true"></i>
            </span>

            <div class="rate col-md-5">
                <m_progress class="mt-4" title="کارگردانی" :percentage="this.percentages[0]"></m_progress>
                <m_progress class="my-3" title="بازیگری" :percentage="this.percentages[1]"></m_progress>
                <m_progress title="فیلم نامه" :percentage="this.percentages[2]"></m_progress>
            </div>

            <div class="img1  mb-4 col-md-2">
                  <i class="fa fa-comments" aria-hidden="true" :style="{color:states[this.status].color}"></i>
            </div>

            <div class="comment_text col-md-5  p-2" >
                <div class="d-flex justify-content-between">
                    <span id="date">{{date}}</span>
                    <div id="title_comment" :style="{color:states[this.status].color}">
                        {{states[this.status].title}}
                    </div>
                    <i id="check1" class="fa fa-check-square" aria-hidden="true" :style="{color:states[this.status].color}"></i>
                </div>

                <div class="d-flex justify-content-center">
                   <span class="comments mt-4 col-11">{{comment}}</span>
                </div>
                <div class="d-flex">
                   <span class=" row col-1 mr-1 mt-5">{{likes}}</span><span class="col-1 mt-5 "><i class="icon_like fa fa-thumbs-up" aria-hidden="true"></i></span>
                    <span class="row col-1 mr-1 mt-5">{{dislikes}}</span><span class="col-1 mt-5"><i class="icon_dislike fa fa-thumbs-o-down" aria-hidden="true"></i></span>
                </div>

            </div>

      </div>
    </div>
</template>

<script>
    import m_progress from './m_progress.vue'
    export default{

        props: ['percentages','date','status','comment','likes','dislikes'],
        components: {
            m_progress
        },
        data(){
            return {
                states:[
                    {
                        title:'نظری ندارم',
                        icon:'fa fa-frown-o',
                        color:'grey'
                    },
                    {
                        title:'پیشنهاد می کنم',
                        icon:'fa fa-frown-o',
                        color:'green'
                    },
                    {
                        title:'پیشنهاد نمی کنم',
                        icon:'fa fa-frown-o',
                        color:'red'
                    },
                ]

            }
        },
        mehtods: {},
        created(){
        }

    }
</script>

<style scoped>
    @import '../assets/main.css';
    @import '../assets/font/font-awesome-4.7.0/css/font-awesome.css';
    @import '../assets/font/font-awesome-4.7.0/css/font-awesome.min.css';
    @import "https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-beta.2/css/bootstrap.min.css";



    .container{
      direction: rtl;
      margin-top: 6vh;
    }


    .comment {
        font-family: Shabnam;
        border: 1px solid #dadbd7;
        border-radius: 7px ;
        position: relative
    }

    .rate{
      font-family: Shabnam;
      font-weight: bold;
    }


    .agree{
        border: 2px solid #1d8030;
    }
    .disagree{
        border: 2px solid #8b120a;
    }

    .star{
        top: -15px;
        right: -16px;
        position: absolute;
    }

    .star i{
        font-size: 22px;
        display: flex;
        justify-content: center;
        align-items: center;
        width: 45px;
        height: 45px;
        color: white;
        border-radius:50% ;
        background-color: #02C06D;
    }
    .comment_text{
        border: 1px solid #dadbd7;
        border-radius: 7px ;
    }

    #date{
      text-align: right;
      font-family: Shabnam;
      font-size: 13px;
      color:grey;
    }

    #title_comment{
      text-align: left;
      font-family: Shabnam;
      font-size: 13px;
      font-weight: bold;
      margin-right: 20vh;
    }

    #check1{
      /*color: #23b24e;*/
      font-size: 1.2em;
    }

  .comments{
    text-align: justify;
    font-family: Shabnam;
    font-weight: bold;
    font-size: 15px;
  }
  .icon_like{
    color: green;
  }

  .icon_dislike{
    color: red;
  }
  .img1{
    font-size: 8em;
  }
</style>
