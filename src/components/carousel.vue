<template>
    <div class="carousel">
        <swiper :options="swiperOption" ref="mySwiper">
        <swiper-slide><img src="../assets/2.jpg" alt=""></swiper-slide>
        <swiper-slide>2</swiper-slide>
        <swiper-slide>3</swiper-slide>
        <swiper-slide>4</swiper-slide>
        <div class="swiper-pagination" slot="pagination"></div>
      </swiper>
    </div>
</template>
<script>
import "swiper/dist/css/swiper.css";
import {swiper,swiperSlide} from "vue-awesome-swiper";
export default {
    name:"carousel",
    components:{
        swiper,
        swiperSlide
    },
    data(){
        return{
            swiperOption:{
            pagination:{
                el:".swiper-pagination",
                dynamicBullets:true
            },
            autoplay:{
                delay:2500,
                disableOnInteraction:false
            }
        }
    };
},
computed:{
    swiper() {
        return this.$refs.mySwiper.swiper;
    }
},
mounted(){
    console.log("this is current instance object",this.swiper);
    this.swiper.slideTo(3,100,false);
    }
};
</script>
<style scoped>
.carousel{
    background:#F7D1D4;
}
</style>


