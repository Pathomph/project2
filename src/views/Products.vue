<template>
  <div class="about">
    <h1>Product List</h1>
    <b-table striped hover 
    :items="products" 
    :fields="fields"
    :per-page="pageSize"
    :current-page="pageIndex"></b-table>
    
  </div>
</template>
<script>
import axios from 'axios'
export default{
    name: 'Products',
    data: function(){
        return{
          message:'Project 2',
          products:[],
          pageSize: 10,
          pageIndex: 1,

          fields: [
            {
              key:'id',
              sortable : true
            },  {
              key:'title',
              sortable : true
            } , {
              key:'price',
              sortable : 'danger'
            }
           
            
              ],


        }
    },
    mounted () {
      var instance = this
    axios
      .get('https://shielded-spire-43023.herokuapp.com/api/products/')
      .then(function(response){
      console.log(response.data)
      instance.products = response.data.data
 })
 },
}

</script>

