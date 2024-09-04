<script setup>

    import {reactive, onMounted} from 'vue';         //REF: alterações em tempo real.

    const user = reactive({
        email:'',
        password:''
    });

    onMounted(() => {
        console.log('componente criado');
    });

    function login(){
        console.log(user.email, user.password);
    }

</script>

<template>

    <form action="" v-on:submit.prevent="login" > 
        <span class="painel" id="painel-text">Login</span>
          
        <div id="email" class="email"><input type="text" placeholder="Email" v-model="user.email"></div>
        <input type="text" placeholder="Senha" v-model="user.password">
        <button type="submit">Login</button>
    </form>

</template>

<style>

    * {
       background-color: rgb(13, 28, 41);
    }

    button {
        color: rgb(0, 0, 0);
        background-color: rgb(255, 255, 255);
    };
    .email {
         margin-bottom: 90px;
    };
    .painel-text {
        color: aqua;
    }
</style>