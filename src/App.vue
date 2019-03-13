<template>
  <div id="app">
    <AppNavbar :data='{jsonObj:titleObj}'/>
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <router-view/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import AppNavbar from '@/components/common/appNavbar'
export default {
  components:{
    AppNavbar
  },
  data(){
    return{
      titleObj:{
        name:"Varsha"
      }
    }
  }

  
}
</script>


<style>

</style>
