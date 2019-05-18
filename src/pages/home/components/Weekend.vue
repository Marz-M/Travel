<template>
  <div>
    <div class="recommend-title">周末去哪</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
          <div class="item-img-wrapper">
        <img
          class="item-img"
          :src="item.imgUrl"
        >
          </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: "HomeWeekend",
  data(){
     return{
          recommendList:[{
          id:'0001',
          imgUrl:'https://h-des-activity-fecp.qunarzz.com/h_des_activity_fe_h_des_activity_fe/161bfb308c31ac5e61afca9b026e7cf4.jpg',
          title:'北京-巴厘岛 5天跟团游',
          desc:'巴厘岛5天【专业摄影师旅拍·Ins网红同款大片+水明漾探店+全程复古老爷车】'
      },
      {
          id:'0002',
          imgUrl:'https://img1.qunarzz.com/vc/b8/25/51/f6173dbd12c1a0f783abe73855.jpg',
          title:'北京-巴厘岛 5天跟团游',
          desc:'巴厘岛5天【专业摄影师旅拍·Ins网红同款大片+水明漾探店+全程复古老爷车】'
      },
      {
          id:'0003',
          imgUrl:'https://h-des-activity-fecp.qunarzz.com/h_des_activity_fe_h_des_activity_fe/8b75ece9943e703fc1b78f2d02a71bae.jpg',
          title:'北京-巴厘岛 5天跟团游',
          desc:'巴厘岛5天【专业摄影师旅拍·Ins网红同款大片+水明漾探店+全程复古老爷车】'
      },]
     }
  }
};
</script>
<style scoped>
.recommend-title {
  line-height: 40px;
  background: #eee;
  text-indent: 10px;
  margin-top: 10px;
}
.item-img-wrapper{
    overflow: hidden;
    height: 0;
    padding-bottom: 30%;
}
.item-img {
  width: 100%;
}
.item-info {
  padding: 5px;
}
.item-title {
  line-height: 27px;
  font-size: 16px;
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}
.item-desc {
  line-height: 20px;
  color: #cccccc;
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}
</style>
