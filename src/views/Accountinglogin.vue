<script>
export default{
    data(){
        return{

        }
    },
    methods:{
        goAccounting(){
            this.$router.push('/Accounting')
        }
    }
}
</script>
<template>
<div class="main">
    <div class="title">
        <h1>Expense Tracker</h1>
    </div>
    <div class="inpText">
        <p>Account</p>
        <input type="text" name="" id="">
        <p>Password</p>
        <input type="text" name="" id="">
    </div>
    <div class="btnBox">
        <button class="btn" type="button">Sign Up</button>
        <button class="btn" type="button" @click="goAccounting()">Log In</button>
    </div>

</div>
</template>
<style scoped lang="scss">
.main{
    margin: 0 auto;
    width: 100vmin;
    height: 100vmin;
    background-color: #161A30;
   .title{
    padding-top: 20vmin;
   }
   .inpText{
    width: 100%;
    height: 20vmin;
    margin-bottom: 2vmin;
   }
   .btnBox{
    width: 100%;
    height: 10vmin;
    /* background-color: aliceblue; */
    .btn{
        margin-top: 10px;
        margin-right: 5vmin;
        background-color: #F0ECE5;
    }
   }
}
</style>