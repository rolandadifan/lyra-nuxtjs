<template>
<div class="homes">
    <Navhome/>
    <b-carousel
      id="carousel-1"
      class="img-corser"
      v-model="slide"
      :interval="4000"
      background="#ababab"
      img-width="1024"
      img-height="480"
      style="text-shadow: 1px 1px 2px #333;"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <!-- Text slides with image -->

      <!-- Slides with custom text -->
      <div img-src="~/assets/home-1.jpg" class="card card-home-custome">
      <div class="recomended-item-home ml-5 mt-3 mr-3">
        <h1 class="tittle-1 mb-3"><i class="far fa-star"></i> Recomended</h1>
        <div class="d-flex">
             <div v-for="music in musics.data" :key="music.id">
                <div class="mr-4">
                    <div class="card card-custome" style="width: 18rem;">
                        <button class="button-home-item"
                        @click="$router.push({
                            name: 'musics-id',
                            params: {id: music.id}
                        })"
                        >
                             <img :src="$axios.defaults.baseURL + '/' + music.thumbnail" height="200" class="card-img-top" alt="...">
                        </button>
                        <div class="card-body">
                            <h5 class="card-title judul">{{ music.judul }}</h5>
                        <p class="card-text penyanyi"> <span>by</span> {{ music.singer }}</p>
                    </div>
                    </div>
                </div>
            </div>
        </div>
      </div>

        <div class="recomended-item-home ml-5  mr-3">
        <h1 class="tittle-1 mb-3"><i class="far fa-location-arrow"></i> New Release</h1>
        <div class="d-flex">
             <div v-for="music in musics.data" :key="music.id">
                <div class="mr-4">
                    <div class="card card-custome" style="width: 18rem;">
                        <button class="button-home-item">
                             <img :src="$axios.defaults.baseURL + '/' + music.thumbnail" height="200" class="card-img-top" alt="...">
                        </button>
                    <div class="card-body">
                        <h5 class="card-title judul">{{ music.judul }}</h5>
                    <p class="card-text penyanyi"> <span>by</span> {{ music.singer }}</p>
                    </div>
                    </div>
                </div>
            </div>
        </div>
        </div>
        <h1 class="tittle-1"></h1>
        
      </div>

      <!-- Slide with blank fluid image to maintain slide aspect ratio -->
    </b-carousel>
    <Footer />
</div>
</template>

<script>
document.addEventListener('contextmenu', event => event.preventDefault());
export default {
     async asyncData({$axios}) {
        const musics = await $axios.$get('/music-goes-on')
        return {musics}
      },
}
</script>
<style scoped>
.card-home-custome{
    background-image: url('~/assets/home-1.jpg');
    background-size: cover;
}
@media screen and (max-width: 1600px) {
    .tittle-1{
        width: 500px;
    }

    .coresel-home-item{
        height: 1000px;
    }
    .card-home-custome{
    height: 1000px;
}
}
.tittle-1{
    margin-right: 1000px;
    margin-top: 15px;
    color: white;
}
.card-custome{
    background-color:rgba(255, 255, 255, 0.5) ;
    margin-bottom:50px ;
}
.card-custome:hover{
    opacity: 0.8;
}
.judul{
    color: whitesmoke;
}
.penyanyi{
    color: grey;
}
.button-home-item{
    border: none;
    background-color:rgba(255, 255, 255, 0.5) ;
}
</style>