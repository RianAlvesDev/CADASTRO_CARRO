<script setup>

    import {ref, reactive, onMounted} from 'vue';         //REF: alterações em tempo real.
 
    const email = ref('');
    const password = ref('');

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

   {{ user.email }}

   <template v-if="user.email.length < 0">Email vazio</template>

    <form action="" v-on:submit.prevent="login" >   
        <input type="text" placeholder="Email" v-model="user.email">
        <input type="text" placeholder="Password" v-model="user.password">
        <button type="submit">Login</button>
    </form>

</template>

<style>
</style>