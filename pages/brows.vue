<template>
    <div>
        <Navhome/>
        <div class="card card-brows-custome">
            <img src="" class="card-img-top" alt="">
            <div class="card-body">
               <Genre />
            </div>
            <div class="card-items-brows mt-5">
                <div class="d-flex justify-content-center mx-3">
                    <div class="card" style="width: 18rem;background-image: linear-gradient(to bottom, #0000ff 0%, #0099ff 100%);">
                        <button @click="submit" style="border:none;background-image: linear-gradient(to bottom, #0000ff 0%, #0099ff 100%);">
                            <h2 class="card-title text-center font-weight-bold">Chill</h2>
                            <img src="~/assets/chill.png" width="200px" class="mx-5 mb-2 image-item">
                        </button>
                    </div>
                    <div class="card ml-3" style="width: 18rem; background-image: linear-gradient(red, white);">
                        <button @click="submit" style="border:none;background-image: linear-gradient(red, white);">
                            <h2 class="card-title text-center font-weight-bold">Indo Music</h2>
                            <img src="~/assets/indomusic.png" width="200px" class="mx-5 mb-2 image-item"> 
                        </button>
                    </div>
                    <div class="card ml-3" style="width: 18rem; background-image: linear-gradient(to bottom, #0000cc 0%, #3366cc 100%);">
                        <button @click="submit" style="border:none;background-image: linear-gradient(to bottom, #0000cc 0%, #3366cc 100%);">
                            <h2 class="card-title text-center font-weight-bold">Instrumenta</h2>
                            <img src="~/assets/instrumenta.png" width="200px" class="mx-5 mb-2 image-item">
                        </button>
                    </div>
                    <div class="card ml-3" style="width: 18rem; background-image: linear-gradient(to bottom, #006699 0%, #66ff66 100%);">
                        <button @click="submit" style="border:none;background-image: linear-gradient(to bottom, #006699 0%, #66ff66 100%);">
                            <h2 class="card-title text-center font-weight-bold">Mood</h2>
                            <img src="~/assets/mood.png" width="200px" class="mx-5 mb-2 image-item">
                        </button>
                    </div>
                </div>
                <div class="d-flex justify-content-center mx-3 mt-4">
                    <div class="card" style="width: 18rem; background-image: linear-gradient(to bottom, #ffcc00 0%, #ff9900 100%);">
                        <button @click="submit" style="border:none;background-image: linear-gradient(to bottom, #ffcc00 0%, #ff9900 100%);">
                            <h2 class="card-title text-center font-weight-bold">Podcast</h2>
                            <img src="~/assets/Podcast.png" width="200px" class="mx-5 mb-2 image-item">
                        </button>
                    </div>
                    <div class="card ml-3" style="width: 18rem; background-image: linear-gradient(to bottom, #ff33cc 0%, #ffccff 100%);">
                        <button @click="submit" style="border:none;background-image: linear-gradient(to bottom, #ff33cc 0%, #ffccff 100%);">
                            <h2 class="card-title text-center font-weight-bold">RnB</h2>
                            <img src="~/assets/rnb.png" width="200px" class="mx-5 mb-2 image-item">
                        </button>
                    </div>
                    <div class="card ml-3" style="width: 18rem;background-image: linear-gradient(to bottom, #6699ff 0%, #99ccff 100%);">
                        <button @click="submit" style="border:none;background-image: linear-gradient(to bottom, #6699ff 0%, #99ccff 100%);">
                            <h2 class="card-title text-center font-weight-bold">Sleep</h2>
                            <img src="~/assets/sleep.png" width="200px" class="mx-5 mb-2 image-item">
                        </button>
                    </div>
                    <div class="card ml-3" style="width: 18rem; background-image: linear-gradient(to bottom, #339966 0%, #669999 100%);">
                        <button @click="submit" style="border:none;background-image: linear-gradient(to bottom, #339966 0%, #669999 100%);">
                            <h2 class="card-title text-center font-weight-bold">Relax</h2>
                            <img src="~/assets/relax.png" width="200px" class="mx-5 mb-2 image-item">
                        </button>
                    </div>
                </div>
        </div>
        </div>
        
        <Footer />
    </div>
</template>

<script>
export default {
    methods: {
    submit(){
       this.$toast.error('Oops...music not available right now')
    }
  }
}
</script>

<style scoped>
    .card-items-brows{
    margin-bottom: 50px;
    }
    .card-brows-custome{
        background-image: url("~/assets/brows.jpg");
        background-size: cover; 
        
    }
    .items-card-brows{
        width: 100px;
    
    }
</style>