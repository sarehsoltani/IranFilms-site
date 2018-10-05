<template>
    <div class="d-flex">
        <div class="col-5 d-flex justify-content-between">
            <span class="" style="color: #007bff">{{this.title}}</span>
            <span class="" style="color: #007bff">{{percentage}} از 10</span>
        </div>

        <div class="col-5">
            <el-progress :percentage="this.percentage*10" :show-text="false" style="width: 200px;">

            </el-progress></div>
    </div>
</template>


<script>
    export default {
        props:['title','percentage'],
        data () {
            return {
                percentage: 40
            }
        },
//
    }
</script>


<style>
    @import "https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-beta.2/css/bootstrap.min.css";
    @import "https://unpkg.com/element-ui/lib/theme-chalk/index.css";
</style>
