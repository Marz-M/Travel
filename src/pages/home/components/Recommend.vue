<template>
  <div>
    <div class="recommend-title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img
          class="item-img"
          :src="item.imgUrl"
        >
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: "HomeRecommend",
  data(){
     return{
          recommendList:[{
          id:'0001',
          imgUrl:'//imgs.qunarzz.com/vs_ceph_vs_tts/9f49524e-c25d-460f-b578-1349af3f9115.jpg_r_480x320x90_a9ba090a.jpg',
          title:'北京-巴厘岛 5天跟团游',
          desc:'巴厘岛5天【专业摄影师旅拍·Ins网红同款大片+水明漾探店+全程复古老爷车】'
      },
      {
          id:'0002',
          imgUrl:'//imgs.qunarzz.com/vs_ceph_vs_tts/9f49524e-c25d-460f-b578-1349af3f9115.jpg_r_480x320x90_a9ba090a.jpg',
          title:'北京-巴厘岛 5天跟团游',
          desc:'巴厘岛5天【专业摄影师旅拍·Ins网红同款大片+水明漾探店+全程复古老爷车】'
      },
      {
          id:'0003',
          imgUrl:'//imgs.qunarzz.com/vs_ceph_vs_tts/9f49524e-c25d-460f-b578-1349af3f9115.jpg_r_480x320x90_a9ba090a.jpg',
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
.item {
  overflow: hidden;
  display: flex;
  height: 94px;
}
.item-img {
  width: 85px;
  height: 85px;
  padding: 5px;
}
.item-info {
  flex: 1;
  padding: 5px;
  min-width: 0;
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
.item-button {
  background: #ff9300;
  padding: 0 10px;
  border-radius: 3px;
  color: #fff;
  line-height: 22px;
  margin-top:8px; 
}
</style>
