<script>
export default{
    data(){
        return{
            obj:[],
            text:"",
            amount:"",
            err:"",
            total:"",
        }
    },
    
    methods:{
        gatMoy(){
            if(this.text==""&&this.amount==""){
                this.err="請確認是否已填寫完畢"
            }
            this.obj.push({text:this.text,amout:this.amount})
            // this.obj.amout=this.amount
            console.log(this.obj);
            console.log(typeof (this.sum));
            

        },
        delinp(){
            this.text=""
            this.amount=""
        },
        delbtn(index){
            this.obj.splice(index,1)
        },
        totalAmount(){
            let sum=0;
            this.obj.forEach(item=>{
                console.log(item.amout);
                sum+=item.amout
            })
            return sum
            
        }
    }
    
}
</script>
<template>
<div class="main">
    <div class="left">
        <div class="title">
            <h1>Expense Tracker</h1>
        </div>
        <div class="userName">
            <h3>Kouhei</h3>
        </div>
        <div class="moy">
            <p>YOUR BALANCE</p>
            <span>${{ totalAmount() }}</span>
        </div>

    </div>
    <div class="right">
        <div class="top">
            <div class="ct">
                <p>INCOME</p>
                <p></p>
            </div>
            <div class="ct">
                <p>EXPENSE</p>
                <p></p>
            </div>
        </div>
        <div class="addBtn">

            <button type="button" class="btn" data-bs-toggle="modal" data-bs-target="#exampleModal" data-bs-whatever="@mdo">Open modal for @mdo</button>

            <button type="button" @click="delinp()" class="btn" data-bs-toggle="modal" data-bs-target="#exampleModal" data-bs-whatever="@mdo">Add transaction</button>

        </div>
        <div class="box" v-for="item in obj">
                <p>{{ item.text }}</p>
                <p>{{ item.amout }}</p>
                <button type="button" class="btn" @click="delbtn">Delete</button>

        </div>

    </div>
</div>

<div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title" id="exampleModalLabel">New message</h5>
        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
      </div>
      <div class="modal-body">
        <form>
          <div class="mb-3">
            <label for="recipient-name" class="col-form-label">Recipient:</label>
            <input type="text" class="form-control" id="recipient-name">
          </div>
          <div class="mb-3">
            <label for="message-text" class="col-form-label">Message:</label>
            <textarea class="form-control" id="message-text"></textarea>
          </div>
        </form>
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
        <button type="button" class="btn btn-primary">Send message</button>
      </div>
    </div>
  </div>
</div>


<!-- 輸入頁 面 -->
<div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog">
    <div class="modal-content">
      
      <div class="modal-body">
        <h1>{{ this.err }}</h1>
        <form>
          <div class="mb-3">
            <label for="recipient-name" class="col-form-label" >Text</label>
            <input type="text" class="form-control" id="recipient-name" v-model="this.text">
          </div>
          <div class="mb-3">
            <label for="message-text" class="col-form-label">Amount</label>
            <input type="number" class="form-control" id="recipient-name" v-model="this.amount">
          </div>
        </form>
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-primary" data-bs-dismiss="modal" @click="gatMoy()">Add transaction</button>
      </div>
    </div>
  </div>
</div>
</template>
<style scoped lang="scss">
.main{
    margin-top: -5px;
    width: 100%;
    height: 100vmin;
    display: flex;
    border: 1px solid black;
    .left{
        width: 30%;
        height: 100%;
        background-color: #161A30;
    }
    .right{
        width: 70%;
        height: 100%;
        background-color: #B6BBC4;
        .top{
            width: 100%;
            height: 30vmin;
            background-color: bisque;
            display: flex;
            .ct{
                margin: 20vmin;
                margin-left: 30vmin;
                font-size: 5vmin;
            }

        }
        .addBtn{
            width: 100%;
            height: 20vmin;
            display: flex;
            justify-content: center;
            align-items: center;
            button{
                background-color: #F0ECE5;
            }
        }
        .box{
            margin-left: 50vmin;
            width: 60vmin;
            height: 10vmin;
            background-color: #161A30;
            display:flex;
            align-items: center;
            p{
                margin-left: 10vmin;
            }
            .btn{
                width: 10vmin;
                height: 5vmin;
                align-items: center;
                margin-left: auto;
                background-color: #F0ECE5;
            }
            
        }
    }
}
.fade{
    color: #161A30;
}
</style>