<template>
    <div class="container">
        <div class="row my-5 align-items-center">
            <div class="col-md-7">
                <h2 class="h1-responsive">
                    I'm <strong>{{ portfolioData.name }}</strong>
                </h2>
                <br><hr><br>
                <p class="text-muted">{{ portfolioData.about }}</p><br>
                <SocialLinks :portfolioData='{portfolioData}'></SocialLinks><br>
                <a href="https://drive.google.com/file/d/14nnlVdbZw5S9s5Uajyn-n3jCblgweo6q/view?usp=sharing" class="btn btn-outline-primary">View Resume</a>
            </div>
            <div class="col-md-5">
                <img src="../../assets/image/varsha.jpg" class="rounded-circle" width="50%" alt="" srcset="">
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


