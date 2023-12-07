<template>
    <div class="box">

    
<div class="title">
    <h1>找質數</h1>
</div>

<div class="main">
    <div class="inpBut">
        <span>找<input type="number" id="key">以內的質數</span>
        <button id="btn" @click="get()">搜　尋</button>
    </div>
    <div class="arrLength">
        <span id="arr"></span>
    </div>
    <div class="num" id="num">

    </div>

</div>
</div>
</template>
<script>

export default {
    methods:{
        get(){
            const arr = document.getElementById("arr");
            const num = document.getElementById("num");
            let n = key.valueAsNumber;
  let arrL = [];

  for (let i = 2; i <= n; i++) {
    let isPrime = true;
    for (let j = 2; j <= Math.sqrt(i); j++) {
      if (i % j == 0) {
        isPrime = false;
        break;
      }
    }
    if (isPrime) {
      arrL.push(i);
    }
  }

  arr.innerText = n + "以內的質數總共:" + arrL.length + "個";
  num.innerText = arrL.join(" , ");

  key.value = " ";
        }
    }
}
</script>
<style scoped lang="scss">
    .box{
    // background-color: #fff;
    margin-left: 25%;

    .title{
        margin-top: 50px;
        display: flex;
        justify-content: center;
        align-items: center;
        width: 800px;
        height: 50px;
        background-color: #fff;
        border-top-left-radius: 10px;
        border-top-right-radius: 10px;
        box-shadow: 5px -4px 25px black;
        color: black;
    }
    .main{
        margin-top: 5px;
        width: 800px;
        height: 500px;
        background-color: #fff;
        border-bottom-left-radius: 10px;
        border-bottom-right-radius: 10px;
        box-shadow: 5px 14px 25px black;
    .inpBut{
        padding: 50px;
        display: flex;
        justify-content: center;
        align-items: center;
        
        span{
            font-size: 20px;
            color: black;
            input{
                width: 150px;
                height: 25px;
                font-size: 20px;
                margin-left: 10px;
                margin-right: 10px;
                color: black;
            }
        }
        button{
            margin-left: 50px;
            width: 70px;
            height: 45px;
            background-color: #712B75;
            color: #fff;
            border-radius: 10px;
            box-shadow: 5px 5px 1px black;
        }
    }
    .arrLength{
        display: flex;
        justify-content: center;
        align-items: center;
        span{
            font-size: 20px;
            color: black;
        }
    }
    .num{
        margin-top: 20px;
        margin-left: 2%;
        margin-right: 20%;
        display: flex;
        border: 1px solid black;
        padding-left: 20px;
        padding-right: 20px;
        padding-top: 10px;
        font-size: 30px;
        overflow-y: scroll;
        width: 47vw;
        height: 40vh;
        color: black;
    }
}
}
</style>