<template>
    <div class="container">
        <div class="row my-5 align-items-center">
            <div class="col-md-3 text-center">
                <img src="../../assets/image/varsha.jpg" class="rounded-circle" width="80%" alt="" srcset="">
            </div>
            <div class="col-md-9 mt-3 d-none d-sm-none d-md-block d-lg-block">
                <h1 class="h1-responsive text-muted font-weight-bold mb-0">{{ portfolioData.name }}</h1>
                <h6 class="text-muted my-0">{{ portfolioData.designation }}</h6>
                <p class="text-muted mt-0"><i>{{portfolioData.description}}</i></p>
                <SocialLinks :portfolioData='{portfolioData}'></SocialLinks>
                <router-link class="btn btn-outline-primary m-0 btn-sm z-depth-0 mt-3" to="about"> About Me </router-link>
            </div>

            <div class="col-md-9 mt-3 text-center d-block d-sm-block d-md-none d-lg-none">
                <h1 class="h1-responsive text-muted font-weight-bold mb-0">{{ portfolioData.name }}</h1>
                <h6 class="text-muted my-0">{{ portfolioData.designation }}</h6>
                <p class="text-muted mt-0"><i>{{portfolioData.description}}</i></p>
                <!-- <SocialLinks class="text-center red" style="text-align:center" :portfolioData='{portfolioData}'></SocialLinks><br> -->
                <router-link class="btn btn-outline-primary m-0 btn-sm z-depth-0" to="about"> About Me </router-link>

                
            </div>
            
        </div>
    </div>
</template>

<script>
import portfolioData from '@/assets/data/portfolioData.json'
import SocialLinks from '@/components/common/socialLinks.vue'

export default {
    components: {
        SocialLinks
    },
    data() {
        return {
            portfolioData
        }
    }
}
</script>


