<template>
<div class="back">
    <img src="../../static/crypto-girl/ranking-background.png" style="    max-height: 100%;
    max-width: 100%;">
    <div class="title-line">
    <div class="title">
         <div class="line"></div>
         <div class="line1"> {{title}}</div>
         <div class="line"></div>
    </div> 
    </div>
    <div class="ranking-ul"> 
     <ul style=" background-color:#97ceea; height: 30px;">
        <li class="rank" style="margin-top: 4px; height: 30px; line-height: 24px;"> <b>名次</b></li> 
        <li class="id" style=" margin-top: 4px; height: 30px;"> ID</li>
        <li class="key" style=" margin-top: 4px; height: 30px;"> 钱包地址</li>
        <li class="time" style=" margin-top: 4px; height: 30px;"> 合成时间</li>   
    </ul>
     </div>
    <div  v-for="( item, index ) in items" :key="item.id" class="ranking-ul"> 
      <ul>
        <li v-bind:id="'ranking'+index" class="rank"> <b>{{ index+1 }}</b></li> 
        <li class="id"> {{ item.ID }}</li>
        <li class="key"> {{ item.key }}</li>
        <li class="time"> {{ item.time }}</li>   
      </ul>
   </div>
</div>
</template>
<script>
export default {
  name: 'rankingList',
   data(){
       return{
        title:"排行榜",
        methods :{
         ranking: function(index){
             return "rank_"+ index
         }
     },
       items: [
      {   ID: 'DanielYang',
      key:'1Eb84h8LnKncKjKLVRztDP2FXE1ixAbXQq',
      time:'2018.0524.18:32' },
      { ID: 'DanielYang',
      key:'1Eb84h8LnKncKjKLVRztDP2FXE1ixAbXQq',
      time:'2018.0524.18:32' },
      { ID: 'DanielYang',
      key:'1Eb84h8LnKncKjKLVRztDP2FXE1ixAbXQq',
      time:'2018.0524.18:32' },
       { ID: 'DanielYang',
      key:'1Eb84h8LnKncKjKLVRztDP2FXE1ixAbXQq',
      time:'2018.0524.18:32' },
       { ID: 'DanielYang',
      key:'1Eb84h8LnKncKjKLVRztDP2FXE1ixAbXQq',
      time:'2018.0524.18:32' },
       { ID: 'DanielYang',
      key:'1Eb84h8LnKncKjKLVRztDP2FXE1ixAbXQq',
      time:'2018.0524.18:32' },
      { ID: 'DanielYang',
      key:'1Eb84h8LnKncKjKLVRztDP2FXE1ixAbXQq',
      time:'2018.0524.18:32' }
    ],
     
   }
 }
}

</script>
<style scoped>
*{
     list-style: none;
}
 .back{
     height: 800px;
     background:no-repeat top center;
     background-color: #f2fcff;
}
.title-line{
     width: 100%;
     display: flex;
     justify-content: center;
}
.title{
     width: 30%;
     height: 50px;
     display: flex;
    justify-content: center 
}
.line{
     width: 25%;
     background-color:#3097cc;
     height: 3px;
     float: left;
     margin-top: 15px;

}
.line1{
     width: 30%;
     height: 42px;
     float: left;
     color:#3097cc;
     font-size: 24px;
}
.tab{
     width: 100%;
     display: flex;
     justify-content: center;
}
.ranking-ul{
     width: 100%;
     height: 60px;
     display:flex;
     justify-content: center
}
.ranking-ul ul{
     height: 60px;
     margin: 0px auto;
     border-bottom: 1px solid #97ceea;
}
 li{  
     text-align: center;
     float:left ;
     font-size: 18px;
}

.rank{
     width: 60px;
     height: 60px;
     line-height: 60px;
}
 .id ,.key,.time{
     margin-top: 25px;
}
.id{
     width: 150px;
     height: 60px;
     margin-top: 25px;
}
.key{
     width: 400px;
     height: 60px;
}
.time{
     width: 200px;
     height: 60px;
}
 .ranking-ul ul:nth-child(even){
     background-color: #ccecf8;
 }

#ranking0{
     background: url(../../static/crypto-girl/Firstplace.png) no-repeat center;
     background-size: 100%;
     font-size: 0;
}
#ranking1{
     
     background: url(../../static/crypto-girl/Secondplace.png) no-repeat center;
     font-size: 0;
     background-size: 100%;
}
#ranking2{
      background: url(../../static/crypto-girl/Thirdplace.png) no-repeat center;
      font-size: 0;
      background-size: 100%;

}

 @media screen and (max-width: 841px) {
     .time{
         display: none;
}
.title{
         width: 50%;
}
 }
  @media screen and (max-width: 665px) {
      .ranking-ul ul{
         width: 80%;
         display: flex;
         justify-content:space-around;
}
     .key{
         display: none;
}
    .rank{
         width: 60px;
         height: 60px;
         line-height: 60px;
}
     .id{
         width: 150px;
         height: 60px;
         margin-top: 25px;
}
     .title{
         width: 80%;
 
}
}
</style>
