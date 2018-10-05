<template>
    <div class="d-flex">
        <div class="col-5 d-flex justify-content-between">
            <span class="" style="color: #007bff">{{this.title}}</span>
            <span class="" style="color: #007bff">{{sliderValue}} از 10</span>
        </div>

          <range-slider
                class="slider"
                min="0"
                max="10"
                step="1"
                v-model="sliderValue">
        </range-slider>

    </div>

</template>

<script>
    import RangeSlider from 'vue-range-slider'
    // you probably need to import built-in style
    import 'vue-range-slider/dist/vue-range-slider.css'

    export default {
        props:['title','value'],
        data () {
            return {
                sliderValue: 0
            }
        },
//        returnValue(){
//            return{
//                 value:this.value
//            }
//        },
        components: {
            RangeSlider
        },

    }
</script>

<style>

    .range-slider-fill{
        background-color: #007bff;

    }
    .slider {

        /* overwrite slider styles */
        width: 250px;
    }

</style>
