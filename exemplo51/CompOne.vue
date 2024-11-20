<template>
    <div>
        <img :src="imgSrc">
        <h2>Component One</h2>
        <p>Choose food.</p>
        <label>
            <input type="radio" name="rbgFood"/> 
            Apple
        </label>
        <label>
            <input type="radio" name="rbgFood"/> 
            Cake
        </label>
    </div>
</template>

<style scoped>
    img {
        float: right;
        height: 100px;
        margin-top: 20px;
    }
    label:hover {
        cursor: pointer;
    }
</style>