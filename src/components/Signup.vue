<template>
<img class="logo" src="./../assets/logo2.jpg" alt="resto logo"/>
    <h1>sign up</h1>

<div class="login">
    <input type="text" placeholder="your name " />
    <input type="text" placeholder="your email " />
    <input type="text" placeholder="your password " />
    <button type="submit">submit</button>
</div>
</template>

<script>
export default{
    name:'SignUp'
}
</script>


<style>
.logo{
    width:320px;
    height:auto
}
.login {
    width: 50%;
    margin: auto;
}

.login input , .login button{
    width: 70%;
    margin: 11px 0px;
    line-height: 2em;
    border: 1px solid #d6d3d3;
    padding: 8px 10px;
    border-radius: 5px;
}


.login button {
    background-color: #df000e;
    color: #fff;
    font-size: 18px;
        width: 75%;
    line-height: 1.5em;
}
</style>