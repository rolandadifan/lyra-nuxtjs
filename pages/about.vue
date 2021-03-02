<template>
    <div>
        <Navhome/>
        <div class="items-about">
        <h1 class="text-white text-center pt-5">About</h1>
        <div class="d-flex justify-content-center ">
            <div class="about-video">
                <iframe width="560" height="350" src="https://www.youtube.com/embed/kKLx43b2BMM" frameborder="0" allow=" autoplay;" allowfullscreen>
                </iframe>
            </div>
            <div class="descriptio">
                <p>
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis ipsam nobis, nostrum dolor impedit distinctio quos, cumque exercitationem minima quo est reiciendis saepe! Quibusdam fugiat quae provident voluptatem porro? Sed!
                </p>
            </div>
        </div>
        </div>
    <Footer/>
    </div>
</template>

<style scoped>
    h1{
        font-size: 48px;
        font-weight: bold;
    }
    .items-about{
        background-image: url('~/assets/home-1.jpg');
        background-size: cover;
        height: 1000px;
    }
    .about-video{
        margin-top: 90px;
    }
    .descriptio{
        width: 500px;
        margin-top: 90px;
    }
    .descriptio p{
        color: white;
        font-size: 24px;
    }
</style>