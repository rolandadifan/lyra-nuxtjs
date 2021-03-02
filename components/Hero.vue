<template>
    <div>
    <b-jumbotron class="hero-home">
        <div class="text-center">
        <h1 class="index-welcome">No Music <br>  &nbsp; &nbsp; &nbsp; &nbsp; No Life</h1>
        <p class="sub-welcome">Find Your Song And Enjoy! </p>
        <nuxt-link to="/home">
            <button class="button-started"> GET STARTED</button>
        </nuxt-link>
        </div>
    </b-jumbotron>
</div>
</template>

<style scoped>
.hero-home{
    margin-top: -20px;
    background-image: url('~assets/photo-1533497197926-c9e810dcea9a.jpg');
    height: 800px;
    background-size: cover;
}
.index-welcome{
    margin-top: 50px;
    font-size: 80px;
    color: #56CB17;
    font-weight: bold;
}
.sub-welcome{
    color: #02D608;
    font-size: 30px;
}
.button-started{
    margin-top: 20px;
    font-size: 24px;
    background-color: #56CB17;
    padding: 10px;
    width: 200px;
    color: white;
    border-radius: 20px;
    box-shadow: #02D608;
    border: none;
}
.button-started:hover{
     background-color: #02D608;
     color: black;
}
</style>