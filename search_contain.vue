<template>
    <div class="body">
        <input v-model="search" type="text" placeholder="...جستجوی فیلم،سریال،بازیگر،کارگردان و غیره"
               class="input text-right"></input>
        <m_button @click="search_method" title="جستجو" ></m_button>
    </div>
</template>
<script>
    import m_button from '../components/m_button.vue'
    export default{
        components: {
            m_button
        },
        data(){
            return {
                search: ''

            }

        },
        methods: {
            test(){

            },
            search_method(){

                const _this = this;
                window.axios.get(`/search/${this.search}`).then(function (result) {

                })

            },


            created(){

            }
        }

    }
</script>
<style scoped>
   @import "../assets/global.css";
   @import '../assets/font/font-awesome-4.7.0/css/font-awesome.css';
  @import '../assets/font/font-awesome-4.7.0/css/font-awesome.min.css';
  @import "https://fonts.googleapis.com/css?family=Roboto:300,400,500,700|Material+Icons";
   @import "https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-beta.2/css/bootstrap.min.css";

    .input {
        color: black;
        background-color: white;
        border-radius: 10px;
        font-family: Shabnam;
        font-size: 15px;
        height: 44px;
        padding-top: 1%;
        padding-right: 2%;
        width: 550px;
    }


</style>
