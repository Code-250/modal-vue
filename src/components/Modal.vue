<template>
    <div class="backdrop">
            <div class="modal">
                <h1>Modal Title</h1>
                <p>modal content and access</p>
            </div>
    </div>
</template>

<style>
    .modal {
        width: 400px;
        padding:20px;
        margin:100px auto;
        border-radius:10px;
        background:white;
    }
    .backdrop {
        top:0%;
        position:fixed;
        width:100%;
        height:100%;
        background:rgba(0,0,0,0.5);
    }
    .modal h1{
        color:rgb(13, 134, 114);
        padding-bottom:10px;
        border-bottom:1px solid #ddd;
    }
    .modal p{
        font-style:normal;
    }
</style>
