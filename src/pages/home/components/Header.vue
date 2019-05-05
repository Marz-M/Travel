<template>
<div class="header">
   <div class="header-left">
       <div class="iconfont back-icon">&#xe624;</div>
   </div>
   <div class="header-input"> <span class="iconfont">&#xe632;</span>输入城市景点游玩主题</div>
   <div class="header-right">
       城市<span class="iconfont arrow-icon">&#xe64a;</span></div>
</div>
</template>

<script>
export default {
name:' HomeHeader'
}
</script>

<style  scoped>
/* @import '~styles/varibles.styl'; */
.header{
    display: flex;
    line-height: 43px;
    background-color: #00bcd4;
    color:#fff;
}
.header-left{
    width: 43px;
    float: left;
}
.back-icon{
    text-align: center;
    font-size: 20px;
}
.header-input{
    flex: 1;
    height: 32px;
    line-height: 32px;
    background: #fff;
    border-radius: 5px;
    margin-top: 6px;
    margin-left: 5px;
    color:#ccc;
    padding-left: 10px;
}
.header-right{
    width: 62px;
    float: right;
    text-align: center;
}
.arrow-icon{
    margin-left: 2px;
    font-size: 12px;
}
</style>



