<template>
  <div class="about">
    <h1>User List</h1>
    <HelloWorld v-bind:msg="message"></HelloWorld>
  </div>
</template>
<script>
import HelloWorld from '@/components/HelloWorld.vue'
export default{
    name: 'Users',
    components: {
        HelloWorld
    },
    data(){
        return{
          message:'Project 2'  
        }
    }
}
</script>
