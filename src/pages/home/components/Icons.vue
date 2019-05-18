<template>
  <div class="icons">
    <swiper>
      <swiper-slide v-for="(page,index) of pages" :key="index">
        <div class="icon" v-for="item of page" :key="item.id">
          <div class="icon-img">
            <img
              class="icon-imgcontent"
              :src='item.imgUrl'
            >
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>
<script>
export default {
  name: "HomeIcons",
  data(){
      return{
          iconList:[{
              id:'0001',
              imgUrl:'https://res.gucci.cn/resources/2019/5/8/15573120135908902_content_LightGray_Vignette_Standard_160x160_1557215103_Vignette_581085XJBIO4318_001_Light.jpg',
              desc:'很多很多很多的小小可爱的卫衣'
          },{
              id:'0002',
              imgUrl:'https://res.gucci.cn/resources/2019/5/8/15573120135904759_content_LightGray_Vignette_Standard_160x160_1557215104_Vignette_581875J1D518516_001_Light.jpg',
              desc:'珠宝'
          },{
              id:'0003',
              imgUrl:'https://res.gucci.cn/resources/2019/5/8/1557312013590295_content_LightGray_Vignette_Standard_160x160_1557215104_Vignette_586028ZAB1R2259_001_Light.jpg',
              desc:'半裙'
          },{
              id:'0004',
              imgUrl:'https://res.gucci.cn/resources/2019/5/8/15573120135904759_content_LightGray_Vignette_Standard_160x160_1557215104_Vignette_581875J1D518516_001_Light.jpg',
              desc:'珠宝'
          },{
              id:'0005',
              imgUrl:'https://res.gucci.cn/resources/2019/5/8/15573120135904759_content_LightGray_Vignette_Standard_160x160_1557215104_Vignette_581875J1D518516_001_Light.jpg',
              desc:'珠宝'
          },{
              id:'0006',
              imgUrl:'https://res.gucci.cn/resources/2019/5/8/15573120135904759_content_LightGray_Vignette_Standard_160x160_1557215104_Vignette_581875J1D518516_001_Light.jpg',
              desc:'珠宝'
          },{
              id:'0007',
              imgUrl:'https://res.gucci.cn/resources/2019/5/8/15573120135904759_content_LightGray_Vignette_Standard_160x160_1557215104_Vignette_581875J1D518516_001_Light.jpg',
              desc:'珠宝'
          },{
              id:'0008',
              imgUrl:'https://res.gucci.cn/resources/2019/5/8/15573120135904759_content_LightGray_Vignette_Standard_160x160_1557215104_Vignette_581875J1D518516_001_Light.jpg',
              desc:'珠宝'
          },{
              id:'0009',
              imgUrl:'https://res.gucci.cn/resources/2019/5/8/15573120135904759_content_LightGray_Vignette_Standard_160x160_1557215104_Vignette_581875J1D518516_001_Light.jpg',
              desc:'珠宝'
          }]
      }
  },
  computed:{
      pages:function(){
          const pages = []
          this.iconList.forEach((item,index) => {
              const page = Math.floor(index / 8)
              if(!pages[page]){
                  pages[page] = []
              }
              pages[page].push(item)
          })
          return pages
      }
  }
};
</script>
<style scoped>
.icons >>> .swiper-container {
  height: 0;
  padding-bottom: 50%;
}
.icons{
  margin-top: 5px;
}
.icon {
  overflow: hidden;
  width: 25%;
  float: left;
  height: 0;
  padding-bottom: 25%;
  position: relative;
}
.icon-img {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 22px;
  box-sizing: border-box;
  padding: 5px;
}
.icon-imgcontent {
  height: 100%;
  display: block;
  margin: 0 auto;
}
.icon-desc {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  height: 22px;
  line-height: 22px;
  color: #333;
  text-align: center;
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}
</style>
