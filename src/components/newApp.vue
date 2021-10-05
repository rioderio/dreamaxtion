<template>
<section class="bg-light pt-5 pb-5 shadow-sm text-dark">
    <div class="container">
        
        <div class="col">
            <div class="row col align-self-start">
                <h3 class="text-left pl-5">Products</h3>
            </div>
            <div class="d-flex justify-content-center border-0 flex-sm-row flex-column col align-self-start">
                <div v-for="val in info" v-bind:key="val.id"> 
                    <div class="card border mr-auto m-4">
                        <div class="card-body border-0">
                            <div class="card-body border-0 custom-a m-3 rounded">
                                <h1 class="card-title col-12">{{ val.id }}</h1>
                            </div>
                        </div>
                        <div class="card-body border-0">
                            <h3 class="card-title text-left m-3">{{ val.name }}</h3>
                            <div class="col d-flex justify-content-center m-0 ">
                                <div class="d-inline-flex p-2 text-left">Total Sold</div>
                                <div class="card-body border-0 m-0 p-2 rounded custom-b">
                                    <h5>{{ val.stock }}</h5>
                                </div>
                            </div>
                                      
                        </div>
                    </div>
                </div>    
            </div>
        </div>
    </div> 
</section>

</template>

<script>
    import axios from 'axios';

    export default {
        name: 'newApp',
        data (){
            return{
                info: {}
            }
        },
        mounted () {
            axios
            .get('https://my-json-server.typicode.com/clementioderio/dreamaxtion/products')
            .then(response => (this.info = response.data))
            .catch(error => console.log(error));
        }   
    }

</script>

<style>
    h3 {
        margin-bottom: 5%;
    }
</style>