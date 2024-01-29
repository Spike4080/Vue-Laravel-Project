<template>
    <form id="signup-form" @submit.prevent="registerUser">
        <label>Name</label>
        <input v-model="formData.name" type="text" required>
        <label>Email</label>
        <input v-model="formData.email" type="text" required>
        <label>Password</label>
        <input v-model="formData.password" type="password" required>
        <button type="submit" class="bg-green-100">Sign Up</button>
    </form>
</template>

<script>
import axios from 'axios';

export default {
    data() {
        return {
            formData: {
                name: '',
                email: '',
                password: ''
            }
        };
    },
    methods: {
        registerUser() {
            axios.post('http://127.0.0.1:8000/api/register', this.formData)
                .then(response => {
                    console.log('Response:', response.data);
                })
                .catch(error => {
                    console.error('Error:', error);
                });
        }
    }
}
</script>


<style>
form {
    background: #fff;
    padding: 20px;
    border-radius: 10px;
    ;
}

label {
    display: block;
    color: #bbb;
    text-transform: uppercase;
    font-weight: bold;
    letter-spacing: 1px;
    font-size: 14px;
    margin: 20px 0 10px 0;
}

input {
    padding: 10px;
    border: 0;
    border-bottom: 1px solid #bbb;
    box-sizing: border-box;
    width: 100%;
}

form button {
    display: block;
    margin: 20px auto 0;
    background: #00ce89;
    color: #fff;
    padding: 10px;
    border: 0;
    border-radius: 6px;
    font-size: 16px;
}
</style>




