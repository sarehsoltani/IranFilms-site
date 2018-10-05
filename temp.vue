<template>
  <div>
    <sare :percentages="[2,10,6]"
                 date="16آبان 1396 23:45:33" status="1" comment=" جالب بود خوشم اومد حتما ببینید " likes="5" dislikes="10"></sare>
  </div>

</template>

<script>
  import sare from './viewpoint.vue'
  export default {

       components:{
            sare,


        }
    }

</script>

<style>


</style>
