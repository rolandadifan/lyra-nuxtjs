<template>
    <div>
        <Navhome/>
        <div class="items-about">
        <h1 class="text-white text-center pt-5">Support US <i class="fas fa-heart"></i></h1>
        <div class="d-flex justify-content-center ">
            <div class="support-email">
               <form>
                  <div class="form-group">
                    <label id="exampleInputEmail1">Email address</label>
                    <input @keyup.enter="userSubscribe" type="email" class="form-control" v-model="subscribe.email">
                </div>
               </form>
            </div>
            <h2 class="text-white" style="margin-top:50px">Or want request music?</h2>
            <div class="request">
              <form action="">
                  <div class="form-group">
                    <label id="exampleInputEmail1">Name</label>
                    <input @keyup.enter="userRequest" type="text" class="form-control" v-model="requestst.name" required>
                </div>
                  <div class="form-group">
                    <label class="mt-3 text-white font-weight-bold req" style="font-size: 24px;">Request your song here</label>
                    <input @keyup.enter="userRequest" type="text" class="form-control" v-model="requestst.request" required>
                </div>
               </form>
            </div>
        </div>
        </div>
    <Footer/>
    </div>
</template>

<script>
export default {
    data(){
        return {
            subscribe:{
                email: ""
            },
            requestst:{
                name: "",
                request: ""
            }
        }
    },
    methods:{
        async userSubscribe(){
            try {
                let response = await this.$axios.$post(
                    '/subscribe', this.subscribe
                )
                console.log(response)
                 this.$toast.success('Successfully subscribe')
            } catch (error) {
                console.log(error)
            }
        },
        async userRequest(){
          try {
              let response = await this.$axios.$post(
                    '/request-music', this.requestst
                )
                console.log(response)
          } catch (error) {
              console.log(error)
          }  
        }
    }
}
</script>

<style scoped>
    .fas{
        color: red;
    }
    h1{
        font-size: 48px;
        font-weight: bold;
    }
    .items-about{
        background-image: url('~/assets/home-1.jpg');
        background-size: cover;
        height: 1000px;
    }
    .support-email{
        width: 400px;
        margin-right: 10px;
    }
    .request{
        width: 400px;
    }
    input{
        border-radius: 20px;
    }
    #exampleInputEmail1{
        color: white;
        font-size: 24px;
        margin-top: 120px;
        font-weight: bold;
    }
</style>