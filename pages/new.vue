<template>
<div class="grid-layouts container text-center">
<div class="row">
<div class="col bg">
    [logo]
</div>
<div class="col bg">
    <ol>
        <li>Home</li>
        <li>About</li>
        <li>Contact</li>
    </ol>
</div>
<div class="col bg">
    <b-button>Register</b-button>
</div>
</div>
<div class="row" style="height: 200px;">
    <div class="col-2 bg">
        Left Sidebar
    </div>
    <div class="col bg">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. 
        Distinctio esse ex labore adipisci, in, illo est beatae nisi placeat ea omnis dicta, 
        explicabo veritatis laboriosam sequi asperiores! Autem, eius ex.
    </div>
</div>
<div class="row">
    <div class="col bg">
        Footer Information
</div>
</div>
</div>
</template>
<script>
export default {
    
}
</script>
<style scoped>
.grid-layouts.container{
    border:1px solid rgb(204,23,17)
}
.bg{
    padding: 10px;
    background-color: #533d7c26;
    border: 1px solid rgba(86,61,124,.2);
}

</style>