<template>
<div class="box">
  <div class="top">
    <span class="iconfont icon-bilibili-line" style="font-size: 12px; margin-top: 2px;"></span>
    <div class="text-left">
    <span> 首页</span>
    <span>番剧</span>
    <span>直播</span>
    <span>游戏中心</span>
    <span>会员购</span>
    <span>漫画</span>
    <span>赛事</span>
    <span class="iconfont icon-a-xiazaikehuduan_huaban1 " style="font-size: 12px;"> 下载客户端</span>
    </div>

    <div class="sousuo">
      <i class="iconfont icon-sousuo"></i>
    <input type="text" placeholder="无衣" style="width: 400px;height: 35px;border-radius: 8px;border: none;padding: 5px;">
    </div>
    <button style="background-color: dodgerblue;color:aliceblue;width: 35px;height:35px;
    border: none;border-radius: 50%;margin-right: 20px;margin-bottom: 125px;">登录</button>

      <div class="icon-list">
        <div v-for="item in icons" :key="item.name" class="icon-group">
        <i :class="'iconfont ' + item.icon"></i>
        <span>{{ item.name }}</span>
        </div>
      </div>

      <button style="background-color: hotpink;
      height: 30px;width:80px;
      border-radius: 8px;color:ghostwhite;
      border: none;font-size: 20px;
      margin-left: 20px;margin-right: 10px;"><span class="iconfont icon-tougaox">投稿</span></button>

      <span class="iconfont icon-bilibili" style="position: absolute;
      left: 90px;bottom: 35px;
      font-size: 40px;"></span>
  
  </div>
  <div class="text2">
    <div class="B1">
      <div class="b1">
       <button class="iconfont icon-fengche " style="padding: 12px;
       background-color:darkorange;color:azure;font-size: 20px;
       border-radius: 50%;border: none;"></button>
       <span>动态</span>
      </div>
      <div class="b1">
       <button class="iconfont icon-remen" style="padding: 12px;
       background-color:crimson;color:azure;font-size: 20px;
       border-radius: 50%;border: none;"></button>
       <span>热门</span>
      </div>
    </div>
    <div class="select">
      <button>番剧</button>
      <button>国创</button>
      <button>综艺</button>
      <button>动画</button>
      <button>鬼畜</button>
      <button>舞蹈</button>
      <button>娱乐</button>
      <button>科技数码</button>
      <button>美食</button>
      <button>汽车</button>
      <button>体育运动</button>
      <button>vlog</button>
      <button>电影</button>
      <button>电视剧</button>
      <button>纪录片</button>
      <button>游戏</button>
      <button>音乐</button>
      <button>影视</button>
      <button>知识</button>
      <button>资讯</button>
      <button>小剧场</button>
      <button>时尚美妆</button>
      <button>动物</button>
      <details class="more-dropdown">
  <summary>
    更多∨ <i class="iconfont icon-arrow-down"></i>
  </summary>
  <div class="dropdown-list">
    <a href=" ">专栏</a >
    <a href="#">活动</a >
    <a href="#">社区中心</a >
    <a href="#">直播</a >
    <a href="#">课堂</a >
    <a href="#">新歌热榜</a >
  </div>
</details>
    </div>
    <div class="right">
      <span class="iconfont icon-zhuanlan"> 专栏</span>
       <span class="iconfont icon-huodong"> 活动</span>
        <span class="iconfont icon-shequzhongxin"> 社区中心</span>
         <span class="iconfont icon-yunzhibo"> 直播</span>
          <span class="iconfont icon-shuben"> 课堂</span>
           <span class="iconfont icon-xingerebang"> 新歌热榜</span>
            
    </div>
  </div>
</div>
</template>

<script setup>
const icons = [
  { name: '大会员', icon: 'icon-svip' },
  { name: '消息', icon: 'icon-xiaoxi1' },
  { name: '动态', icon: 'icon-fengche' },
  { name: '收藏', icon: 'icon-shoucang-weishoucang' },
  { name: '历史', icon: 'icon-history' },
    { name: '创作中心', icon: 'icon-iconfinder_m-_' },
]
</script>

<style>
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.box{width: 10o0vw;
  height: 100vh;
  background-color: black;
}
.top {position: relative;
  display: flex;
  padding: 10px;
  color:#ffffff;
  width: 100%;
  height: 140px;
  background-image: url(/src/assets/back.jpg);
  background-size:100% 100%;
}
.text-left{
  display: flex;
  font-size: 12px;
  gap:20px;
}
.text2{height: 90px;
  width: 100%;
 background-color: #ffffff;
 position: relative;
}
.sousuo{
  color: #1c1b1b;
  flex: 1;
  display: flex;
  justify-content: center;
  position: relative;
}
.sousuo i{
  position: absolute;
  top:8px;
  right: 100px;
  font-size: 18px;
 
}
.icon-list{display: flex;
gap: 20px;
font-size: 10px;}
.icon-group{display: flex;
flex-direction: column;
align-items:center;}
.B1{
  display: flex;
  gap: 20px;
  position: absolute;
  top:15px;left: 100px;
}
.b1{
  display: flex;
  flex-direction: column;
  gap: 3px;
  font-size: 10px;
  align-items: center;
}
.select{
  display: flex;
  position: absolute;
  top: 15px;left:240px;
  flex-wrap: wrap;
  width: 850px;
  gap:5px;
border-right:1px solid #757070;
}
.select button{
  padding: 3px;
  width: 65px;
  height: 25px;
  line-height: 1;
  border: none;
  font-weight: 300;
  border-radius: 5px;
}
.more-dropdown {
  position: relative;
  display: inline-block;
}

summary {
  cursor: pointer;
  display: flex;
  align-items: center;
  background-color: #f0efef;
  border-radius: 5px;
  width: 65px;height: 25px;
  padding: 3px;
  font-weight:300;font-size: 13px;
  line-height: 1;

}


.dropdown-list {
  position: absolute;
  top: 100%;
  left: 0;
  background-color: #fff;
  border: 1px solid #e5e5e5;
  border-radius: 8px;
  padding: 8px 0;
  min-width: 100px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
  z-index: 10;
  display: flex;
  flex-direction: column;
}

.dropdown-list a {
  display: block;
  padding: 8px 16px;
  color: #333;
  text-decoration: none;
  white-space: nowrap;
}

.dropdown-list a:hover {
  background-color: #f5f5f5;
}
.right{
  position: absolute;
  right: 80px;
  margin: 20px;
  width: 210px;height:90px;
}
.right span{
  margin: 10px;
  font-size: 12px;
  color: #444242;
}
</style>