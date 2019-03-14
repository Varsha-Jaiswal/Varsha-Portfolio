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
    <AppFooter></AppFooter>
  </div>
    
</template>

<script>
import AppNavbar from '@/components/common/appNavbar'
import AppFooter from '@/components/common/appFooter'
export default {
  components:{
    AppNavbar,
    AppFooter
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
