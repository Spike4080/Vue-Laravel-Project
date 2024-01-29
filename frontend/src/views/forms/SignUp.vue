<template>
  <form>
    <label>Email</label>
    <input type="text" required>
    <label>Password</label>
    <input type="password" required>
    <button>Sign Up</button>
  </form>
</template>

<script>
export default {
}
</script>

<style>
    form {
        background: #fff;
        padding: 20px;
        border-radius: 10px;;
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