<template>
  <div class="wrapper">
    <swiper :options="swiperOption" v-if="showSwiper">
    <!-- slides -->
    
    <swiper-slide v-for="item of list" v-bind:key=item.id>
        <img class="swiper-img" :src="item.imgUrl" alt="江西三清山">
    </swiper-slide>
    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
  </div>
</template>
<script>
export default {
    name:'HomeSwiper',
    props:{
        list:Array
    },
    data:function(){
        return{
            swiperOption: {
                pagination:'.swiper-pagination',
                loop:true,
            },
            
        }
    },
    computed:{
        showSwiper(){
            return this.list.length
        }
    }
}
</script>
<style scoped>
.wrapper{
    width: 100%;
    height: 0;
    overflow: hidden;
    padding-bottom: 31.8%;
    background: #eee;
    /* height: 37.05vm; */
}
.swiper-img{
    width: 100%;
}
.wrapper >>> .swiper-pagination-bullet-active{
    background: #fff;
}
</style>
