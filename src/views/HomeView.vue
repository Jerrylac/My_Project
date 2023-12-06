<script setup></script>

<template>
  <div class="flipBox">

    <div class="flip1">
      <div class="front" style="
          background-image: url(https://media.discordapp.net/attachments/483550384133111808/1166774573275029616/chihuahua-smile.gif?ex=654bb67f&is=6539417f&hm=78c84357c72c0e87d184405d55ab6b876b443a192adb97ad1e85f97f3715a7e1&);
        ">
        <!-- <h1 class="text-shadow">預定照片</h1> -->
      </div>
      <div class="back" style="background-image: url(https://media4.giphy.com/media/TcdpZwYDPlWXC/giphy.gif);">
        <!-- <p>預定照片</p> -->
      </div>
    </div>
  </div>
  <div class="flipBoxT">
    <div class="flip">
      <div class="front" style="background-image: url();">
        <div class="userT">
          <i class="fa-solid fa-user-large"></i>
          <h1 class="text-shadow">關於我</h1>
        </div>
      </div>
      <div class="back">
        
          <h2>Angular</h2>
          <p>我畢業於樹德科技大學在學期間中參加過學生會在其中擔任過活動的組長，課餘期間有時也會去學習不同的東西，在工作期間我負責的職務快速的處理完畢，若是有心人也會去教導他們怎麼快速的操作</p>
          <hr>
        
      </div>
    </div>
    <div class="flip">
      <div class="front" style="">
        <div class="bockT">
          <i class="fa-brands fa-readme"></i>
          <h1 class="text-shadow">學習經歷</h1>
          
        </div>
      </div>
      <div class="back">
        <div class="text">
          <h4>學歷</h4>
        <p>
          大學:樹德科技⼤學
        </p>
          <p>
            學系:資訊管理
          </p>
          <p>
            畢業時間:2021年6⽉
          </p>
          <h5>在學期間:</h5>
          <p>參加學⽣會活動的組⻑活動⾏中學到團隊構的重性</p>
          <hr>
          <h4>進修經歷</h4>
          <p>瑋育TibaMe就業養成班THM101</p>
          <p>微軟全端開發養成</p>
          <p>2023年2月~6月</p>
          <p>進修期間學習JavaScript、CSS、HTML、bootstrap、vue、C#、ASP.NET MVC以及MS SQL的操作</p>
          <p>bootstrap以及vue是使用cdn的方式操作</p>
          <p>-----------------</p>
        </div>
        
      </div>
    </div>
    <div class="flip">
      <div
        class="front"
        style="
          
        "
      >
      <div class="workI">

        <i class="fa-solid fa-briefcase"></i>
        <h1 class="text-shadow"> 工作經歷</h1>
      </div>
      </div>
      <div class="back">
        
          <h4>工作經歷</h4>
          <p>
            康洋生技國際有限公司|客服人員
          </p>
          <p>2020/9 –2023/7</p>
          <h5>工作內容</h5>
          <p>協助客人訂單上的問題系統</p>
          <p>出現問題時及時聯繫技術處理該問題</p>
        
      </div>
    </div>

  </div>
  
  <!-- <a href="https://mythrillfiction.com/" target="_blank">Mythrill</a> -->
</template>
<style scoped lang="scss">
  h1 {
    font-size: 2.2em;
    color: #000;
    text-shadow: 0px 0px 5px white;
  }
.flipBoxT{
  width: 85vw;
  height: 85vmin;
// background-color: azure;
// padding-left: 7vmin;
  .flip {
    margin-top: 50px;
    margin-left: 11vmin;
    position: relative;
    .front,
    .back {
      display: block;
      transition-timing-function: cubic-bezier(0.175, 0.885, 0.32, 1.275);
      transition-duration: 0.5s;
      transition-property: transform, opacity;
      .text{
        width: 100%;
        height: 100%;
        overflow-y: scroll;
        
      }
      .text::-webkit-scrollbar{
        width: 10px;
      }
      .text::-webkit-scrollbar-track {
        background: #3b73b8;
        border-radius: 10px;
      }
      .text::-webkit-scrollbar-thumb {
        background: #aec3d7;
        border-radius: 10px;
      }
      .text::-webkit-scrollbar-thumb:hover {
  background: #fff;
}

    }
    .front {
      transform: rotateY(0deg);
    }
    .back {
      position: absolute;
      opacity: 0;
      top: 0px;
      left: 0px;
      width: 100%;
      height: 100%;
      transform: rotateY(-180deg);
    }
    &:hover {
      .front {
        transform: rotateY(180deg);
      }
      .back {
        opacity: 1;
        transform: rotateY(0deg);
      }
    }
    &.flip-vertical {
      .back {
        transform: rotateX(-180deg);
      }
      &:hover {
        .front {
          transform: rotateX(180deg);
        }
        .back {
          transform: rotateX(0deg);
        }
      }
    }
  }
  .flip {
    position: relative;
    display: inline-block;
    width: 42vmin;
    .front,
    .back {
      box-shadow: 5px 5px 5px black;
      display: block;
      color: white;
      width: 50vmin;
      background-size: cover !important;
      background-position: center !important;
      height: 80vmin;
      padding: 1em 2em;
      background: #313131;
      border-radius: 10px;
      background-color: #4D3C77;
      p {
        font-size: 1rem;
        line-height: 160%;
        color: white;
        font-weight: bold;
      }
    }
    .workI{
      margin-top: 50%;
      .fa-briefcase{
        font-size: 5vmin;
        display: flex;
        justify-content: center;
      }
      h1{
        margin-top: 20px;
        font-size: 2.2em;
        color: #000;
        text-align: center;
        text-shadow: 0px 0px 5px white;
      }
    }
    .bockT{
      margin-top: 50%;
      .fa-readme{
        font-size: 5vmin;
        display: flex;
        justify-content: center;
      }
      h1{
        margin-top: 20px;
        font-size: 2.2em;
        color: #000;
        text-align: center;
        text-shadow: 0px 0px 5px white;
      }
    }
    .userT{
      margin-top: 50%;
      .fa-user-large{
        font-size: 5vmin;
        display: flex;
        justify-content: center;
      }
      h1{
        margin-top: 20px;
        font-size: 2.2em;
        color: #000;
        text-align: center;
        text-shadow: 0px 0px 5px white;
      }
    }
  }
}

.flipBox{
  
  margin-left: 13vmin;
  width:100vmin;
  height: 60vmin;
  border-bottom: 2px solid black;
  // background-color: #fff;
  .flip1 {
    margin-top: 50px;
    // margin-left: 10vmin;
  
    position: relative;
    .front,
    .back {
      display: block;
      transition-timing-function: cubic-bezier(0.175, 0.885, 0.32, 1.275);
      transition-duration: 0.5s;
      transition-property: transform, opacity;
    }
    .front {
      transform: rotateY(0deg);
    }
    .back {
      position: absolute;
      opacity: 0;
      top: 0px;
      left: 0px;
      width: 100%;
      height: 100%;
      transform: rotateY(-180deg);
    }
    &:hover {
      .front {
        transform: rotateY(180deg);
      }
      .back {
        opacity: 1;
        transform: rotateY(0deg);
      }
    }
    &.flip-vertical {
      .back {
        transform: rotateX(-180deg);
      }
      &:hover {
        .front {
          transform: rotateX(180deg);
        }
        .back {
          transform: rotateX(0deg);
        }
      }
    }
  }
  .flip1 {
    position: relative;
    display: inline-block;
    width: 40vmin;
    .front,
    .back {
      box-shadow: 5px 5px 5px black;
      display: block;
      color: white;
      width: inherit;
      background-size: cover !important;
      background-position: center !important;
      height: 40vmin;
      padding: 1em 2em;
      background: #313131;
      border-radius: 50%;
      p {
        font-size: 0.9125rem;
        line-height: 160%;
        color: #999;
      }
    }
  }

}
</style>
