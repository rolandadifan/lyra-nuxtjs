<template>
    <div>
        <Navhome/>
        <div class="card card-id-custome">
            <div class="row d-flex">
                <div class="imag-border">
                    <img :src="$axios.defaults.baseURL + '/' + musics.data.thumbnail" class="card-img-top img-detail" alt="">
                </div>
                <div class="detail-info">
                    <h2 class="title-detail">Songs</h2>
                    <h1 class="judul-detail">{{ musics.data.judul }}</h1>
                    <h5><i class="fas fa-music"></i> {{ musics.data.singer }}  <span> <i class="far fa-calendar-alt"></i> {{ musics.data.year }}   <i class="far fa-clock"></i> {{ musics.data.duration }} </span></h5>
                    <p>{{ musics.data.genre }}</p>
                </div>
            </div>
            <div class="card-body">
                <div class="d-flex justify-content-center">
                <audio controls class="audio-custome">
                    <source :src="musics.data.music">
                </audio>
                </div>
            </div>
        </div>
        <Footer />
    </div>
</template>

<script>
export default {
    async asyncData({ $axios, params}) {
        const musics = await $axios.$get('music-goes-on/' + params.id)
        return {musics}
    },
}
</script>

<style scoped>
    .card-id-custome{
        margin-bottom: 35px;
        background-image: url('~/assets/wallpaper.gif');
        
    }
    .img-detail{
        width: 500px;
        margin: 20px;
    }
    .imag-border{
        margin: 20px;
    }
    .detail-info{
        margin-top: 30px;
        color:white;
    }
    .judul-detail{
        font-size: 48px;
        font-weight: bold;
        color: white;
    }
    .audio-custome{
        margin-top: 100px;
        width: 1000px;
    }
    audio::-webkit-media-controls-panel {
                background-color: gray;
    }
</style>