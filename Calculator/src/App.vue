
<template>
    <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>  
    <div class="container">
        <div class="calculator">
            <form>
                <div class="display">
                    <input type="text" name="display" v-bind:value="current" readonly>
                </div>
                <div class="row1">
                    <input type="button" value="%">
                    <input type="button" value="CE">
                    <input type="button" value="C">
                    <input type="button" value="del">
                </div>
                <div class="row2">
                    <input type="button" value="1/x">
                    <input type="button" value="x²">
                    <input type="button" value="√x">
                    <input type="button" value="÷">
                </div>
                <div class="row3">
                    <input type="button" value="7">
                    <input type="button" value="8">
                    <input type="button" value="9">
                    <input type="button" value="x">
                </div>
                <div class="row4">
                    <input type="button" value="4">
                    <input type="button" value="5">
                    <input type="button" value="6">
                    <input type="button" value="-">
                </div>
                <div class="row5">
                    <input type="button" value="1">
                    <input type="button" value="2">
                    <input type="button" value="3">
                    <input type="button" value="+">
                </div>
                <div class="row6">
                    <input type="button" value="+/-">
                    <input type="button" value="0">
                    <input type="button" value=".">
                    <input type="button" value="=">
                </div>
            </form>
        </div>
    </div>
</body>
</html>
</template>
<style scoped>
.container{
    width: 100%;
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
}
.calculator{
    background: #040e27;
    padding:20px;
    border-radius: 10px;
}
.calculator form input{
    border:2px solid #fff;
    border-radius: 10px;
    width: 60px;
    height:60px;
    box-shadow: -8px -8px 15px rgba(255,255,255,0.1),5px 5px 15px rgba(0,0,0,0.2);
    background:transparent;
    font-size: 20px;
    color: #fff;
    cursor: pointer;
    margin:10px;
}
.display{
    display: flex;
    justify-content: flex-end;
    margin: 20px 0;

}
form .display input{
    text-align: right;
    flex:1;
    font-size: 45px;
    box-shadow: none;
}


</style>


<script>
  export default{
    data(){
      return{
        current:'0',
      }
    },
    methods:{
      clear(){
        this.current='';
      }
    }
  }
</script>