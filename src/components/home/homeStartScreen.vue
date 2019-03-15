<template>
    <div class="container">
        <div class="row my-5 align-items-center">
            <div class="col-md-7">
                <h1 class="h1-responsive text-muted font-weight-bold">{{ portfolioData.name }}</h1>
                <h6 class="text-muted">{{ portfolioData.designation }}</h6>
                <ul class="list-group list-group-horizontal" type="none">
                    <li v-for="(item, i) in portfolioData.socialMediaProfiles" :key="i">
                        <a :href="item.url" target="_blank" class="fb-ic mr-3" style="color:black; " role="button">
                            <i :class="item.icon"></i>
                        </a>
                    </li>
                </ul>
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


