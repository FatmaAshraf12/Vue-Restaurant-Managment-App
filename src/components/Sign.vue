<template>
<img class="logo" src="./../assets/logo2.jpg" alt="resto logo"/>
    <h1>sign up</h1>

<div class="login">
    <input type="text" v-model="name" placeholder="your name " />
    <input type="text" v-model="email" placeholder="your email " />
    <input type="password" v-model="password" placeholder="your password " />
    <button v-on:click="SignUp">submit</button>
</div>
</template>

<script>
import axios from 'axios'
export default{
    name:'SignUp',
    data(){
        return{
            name:'',
            email:'',
            password:''
        }
    },
    methods:{
        async SignUp(){
            let result = await axios.post("http://localhost:3000/user",{
                email:this.email,
                password:this.password,
                name:this.name
            });
            console.warn(result);
            if(result.status == 201){
            alert("sign up done");
            localStorage.setItem("user-info",JSON.stringify(result.data))
            }

        }
    }
   
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
        width: 73%;
    line-height: 1.5em;
}
</style>