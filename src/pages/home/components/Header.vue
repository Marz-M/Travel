<template>
<div class="header">
   <div class="header-left">返回</div>
   <div class="header-input">输入城市景点游玩主题</div>
   <div class="header-right">城市</div>
</div>
</template>

<script>
export default {
name:' HomeHeader'
}
</script>

<style  scoped>
.header{
    display: flex;
    line-height: 43px;
    background-color: #00bcd4;
    color:#fff
}
.header-left{
    width: 43px;
    float: left;
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
}
.header-right{
    width: 62px;
    float: right;
    text-align: center;
}
</style>



