<template>
    <div class="page-container">
        <div class="login-container">
            <button id=" btn" @click="login()">Click here</button>
        </div>
    </div>
</template>

<script>
// import Store from "../vuex/store.js";

// import "vue3-toastify/dist/index.css";
import axios from "axios";

export default {
    // authSource: '',
    name: 'GitHub',
    methods: {
       
        async login() {
            try {
                const response = await axios.get("https://github.com/login");
                console.log(`success`);
                console.log(response);
            } catch (error) {
                console.error("Login failed:", error);
            }
        }
    }
}
</script>

<style scoped>
body {
    font-family: Arial, sans-serif;
    background-color: #f0f0f0;
    margin: 0;
}

.page-container {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 80vh;
    padding: 20px;
}

.login-container {
    background-color: white;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    text-align: center;
    width: 100%;
    max-width: 900px;
}

.login-container h2 {
    margin-bottom: 20px;
}

.login-btn {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 50%;
    padding: 10px;
    margin: 10px auto;
    border: 1px solid transparent;
    border-radius: 7px;
    font-size: 16px;
    cursor: pointer;
    color: black;
    text-align: left;
}

.login-icon {
    width: 20px;
    height: 20px;
    margin-right: 8px;
}


.microsoft-btn {
    border-color: black;
    background-color: white;
}

.github-btn {
    background-color: white;
    border-color: #333;
}

.linkedin-btn {
    background-color: white;
    border-color: black;
}

.favicon {
    height: 30px;
    width: 30px;
}

.login-btn:hover {
    opacity: 0.9;
}
</style>