<template>
  <div>
    <div class="recommend-title">周末去哪</div>
    <ul>
      <li class="item border-bottom" v-for="item of list" :key="item.id">
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
  props:{
    list:Array
  }
};
</script>
<style scoped>
.recommend-title {
  line-height: 40px;
  background: #eee;
  text-indent: 10px;
}
.item-img-wrapper{
    overflow: hidden;
    height: 0;
    padding-bottom: 38%;
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
