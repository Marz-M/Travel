<template>
  <div class="wrapper">
    <swiper :options="swiperOption" >
    <!-- slides -->
    
    <swiper-slide v-for="item of swiperList" v-bind:key=item.id>
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
    data:function(){
        return{
            swiperOption: {
                pagination:'.swiper-pagination',
                loop:true,
            },
            swiperList:[{
                id:'0001',
                imgUrl:'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/312dce00477e3db8672f2ca46fdb42df.jpg_890x330_a802c59b.jpg',
            },{
                id:'0001',
                imgUrl:'https://imgs.qunarzz.com/piao/fusion/1605/25/937e0c04d5f7e1f7.jpg_890x330_ce8fba37.jpg'
            }
            ]
        }
    }
}
</script>
<style scoped>
.wrapper{
    width: 100%;
    height: 0;
    overflow: hidden;
    padding-bottom: 37.07%;
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
