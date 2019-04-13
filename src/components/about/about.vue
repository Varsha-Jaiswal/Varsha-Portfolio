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
                <a href="https://drive.google.com/open?id=1EK93zj3xTIvnqf8ThUaqmEcSTE3e0jWT" target="_blank" class="btn btn-outline-primary">View Resume</a>
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


