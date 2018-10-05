<template>
  <div>
    <header1 class="head1"></header1>
    <movie_detail :MovieTitle="detail_res.original_title"  :rate="detail_res.rate" :year="detail_res.year" :length="detail_res.length" :director="detail_res.director" :description="detail_res.description" :country="detail_res.country" :authors="detail_res.authors" :stars="detail_res.stars"></movie_detail>
    <downloadbar class="downbar"></downloadbar>
    <comment></comment>
     <downloadrate></downloadrate>
    <!--<viewpoint></viewpoint>-->
    <!--//   props: ['percentages','date','status','comment','likes','dislikes'],-->
    <viewpoint  v-for="(res,index) in comment_res" :percentages="[res.rate_director,res.rate_actor,res.rate_film]"  :key="index"
                 :date="res.created_at" status="1" :comment="res.comment" likes="5" dislikes="10"></viewpoint>
    <!--<viewpoint :percentages="[2,10,6]"-->
                     <!--date="16آبان 1396 23:45:33" status="1" comment=" جالب بود خوشم اومد حتما ببینید " likes="5" dislikes="10"></viewpoint>-->
    <!--<viewpoint  :percentages="[comment_res.rate_director,comment_res.rate_actor,comment_res.rate_film]"-->
                 <!--:date="comment_res.created_at" status="1" :comment="comment_res.comment" likes="5" dislikes="10"></viewpoint>-->

    <!--<viewpoint :percentages="[2,10,6]"-->
                     <!--date="16آبان 1396 23:45:33" status="2" comment=" جالب بود خوشم اومد حتما ببینید " likes="5" dislikes="10"></viewpoint>-->

    <m_footer></m_footer>
  </div>
</template>

<script>
import header1 from '../components/header1.vue'
import movie_detail from '../components/movie_detail.vue'
import downloadbar from '../components/downloadbar.vue'
import viewpoint from '../components/viewpoint.vue'
import downloadrate from '../components/downloadrate.vue'
import comment from '../components/comment.vue'
import m_footer from '../components/m_footer.vue'

export default {
  data(){
            return{
                id:1,//From user
                comment_res:[],
                detail_res:[],

            }
        },
        created(){
            const _this = this;
            window.axios.get(`/movies/${this.id}/comments`).then(function(result){
                _this.comment_res = result.data;
                console.log(_this.comment_res)
            })


            window.axios.get(`/movies/${this.id}/details`).then(function(result){
                _this.detail_res = result.data[0];
                console.log(_this.detail_res)
            })
        },

   components: {
     header1,
     m_footer,
     movie_detail,
     downloadbar,
     viewpoint,
     comment,
     downloadrate,
    }
  }
</script>

<style scoped>
  @import '../assets/main.css';
  @import '../assets/font/font-awesome-4.7.0/css/font-awesome.css';
  @import '../assets/font/font-awesome-4.7.0/css/font-awesome.min.css';
  @import "//maxcdn.bootstrapcdn.com/font-awesome/4.1.0/css/font-awesome.min.css";
  @import "https://fonts.googleapis.com/css?family=Roboto:300,400,500,700|Material+Icons";

  .head1{
    margin-bottom: 12vh;
  }
  .downbar{
    margin-top: 8vh;
  }


</style>
