<template>
    <div class="main">
      <div class="box">
        <div class="title">
          <h1 id="box">猜一個數字</h1>
        </div>
        <div class="numr" id="r1">
            <div class="text">
                <h1 id="floor">1</h1>
                <h2 id="ans">－</h2>
                <h1 id="top">100</h1>
            </div>
        </div>
        <div class="cs1">

            <h4 id="b1">您只有5次機會</h4>
        </div>
        <div class="inp">
          <input type="number" name="" id="random" />
        </div>
        <button id="btn" @click="get()">回答</button>
      </div>
    </div>
</template>
<script>
export default {
    methods:{
        get(){
            const random = document.getElementById("random");
const box = document.getElementById("box");
const floor = document.getElementById("floor");
const topNum = document.getElementById("top");
const ans = document.getElementById("ans");
const btn = document.getElementById("btn");
const b1=document.getElementById("b1")
let randomNum = Math.floor(Math.random() * 97) + 2;
console.log(randomNum);
// 最大最小值
let smaNum = 1;
let bigNum = 100;
// 剩餘次數
let a = 0;
let b = 5;

btn.addEventListener("click", function () {
  const text = random.valueAsNumber;
  const flo = parseInt(floor);
  const top = parseInt(topNum);

  a++;
  b--;
    b1.innerText="您還有"+b+"次機會"
  if (text < smaNum || text > bigNum) {
    box.innerText =
      "請輸入介於" + smaNum + "~" + bigNum + "的數字" + "剩下次數為" + b;
  } else if (text == randomNum) {
    box.innerText = "你答對了";
    floor.innerText = "";
    topNum.innerText = "";
    ans.innerText = "數字為：" + text;
  } else if (text < randomNum) {
    box.innerText = "你猜小了剩餘次數" + b;
    floor.innerText = text;
    smaNum = text;
  } else if (text > randomNum) {
    box.innerText = "你猜大了剩餘次數" + b;
    topNum.innerText = text;
    bigNum = text;
  }
  if (a == 5) {
    box.innerText = "已超過5次請從新再來";
    b1.innerText=" "
    random.disabled = true;
  }
  
  random.value = "";
});

        }
    }
}
</script>
<style scoped lang="scss">
    .main{
    width: 500px;
    height: 500px;
    background-color: #fff;
    border-radius: 20px;
    box-shadow: 0px 0px 40px rgb(31, 31, 31);
    margin: 0 auto;
    margin-top: 100px;
    display: flex;
    justify-content: center;
    align-items: center;
    .box{
        width: 75%;
        height: 75%;
        .title{
            width: 100%;
            height: 30%;
            display: flex;
            justify-content: center;
            align-items: center;
            color: black;
        }
        .numr{
            width: 100%;
            height: 30%;
            display: flex;
            justify-content: center;
            align-items: center;
            .text{
                display:flex;
                justify-content: center;
                align-items: center;
                color: black;
            }
        }
        h4{
            margin-bottom: 0px;
        }
        .inp{
            width: 100%;
            height: 10%;
            display: flex;
            justify-content: center;
            align-items: center;
            input{
                width: 200px;
                height: 20px;
                color: black;
            }
        }
        button{
            width: 100px;
            height: 30px;
            border-radius: 10px;
            margin-left: 35%;
            background-color: #6B728E;
            color: #fff;
        }
    }
    .cs1{
        display: flex;
        justify-content: center;
        align-items: center;
        color: black;
    }
}
</style>