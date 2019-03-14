<template>
    <div class="container">
        <div class="row red my-5 align-items-center">
            <div class="col-md-5 green">
                <img src="https://gdgjalandhar.com/img/varsha.380e53ce.jpg" class="rounded-circle" width="50%" alt="" srcset="">
            </div>
            <div class="col-md-7 yellow">
                <h3 class="h3-responsive">{{ portfolioData.name }}</h3>
                <p class="text-muted">{{ portfolioData.designation }}</p>
                <p class="text-muted">Social links logos</p>
                <button class="btn btn-primary p-2">See more</button>
            </div>
        </div>
    </div>
</template>

<script>
import portfolioData from '@/assets/data/portfolioData.json'
export default {
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


