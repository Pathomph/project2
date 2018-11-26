<template>
  <div class="about">
    <h1>Product List</h1>
    <HelloWorld v-bind:msg="message"></HelloWorld>
  </div>
</template>
<script>
import axios from 'axios'
export default{
    name: 'Products',
    data(){
        return{
          message:'Project 2'  
        }
    },
    mounted () {
    axios
      .get('https://shielded-spire-43023.herokuapp.com/api/products/')
      .then(function(response))
      console.log(response.data)
  }
})
}
</script>

