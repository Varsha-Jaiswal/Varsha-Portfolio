<template>
    <div class="container">
        <div class="row my-5 align-items-center">
            <div class="col-md-7">
                <h1 class="h1-responsive text-muted font-weight-bold">{{ portfolioData.name }}</h1>
                <h6 class="text-muted">{{ portfolioData.designation }}</h6>
                <SocialLinks :portfolioData='{portfolioData}'></SocialLinks>
                <router-link class="btn btn-outline-primary" to="about"> About Me </router-link>
            </div>
            <div class="col-md-5">
                <img src="https://gdgjalandhar.com/img/varsha.380e53ce.jpg" class="rounded-circle" width="50%" alt="" srcset="">
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
    methods: {
        showData() {
            this.$emit('ShowGitHubData')
        }
    },
    data() {
        return {
            portfolioData
        }
    }
}
</script>


