<template>
    <div class="container-fluid">
        <hr><br>  
        <h3>Tech Talks</h3>
        <br><hr>
        <div class="row">
            <div class="col-md-6" v-for="(item, i) in homePageTalks" :key="i"> 
                <div class="card m-2">
                    <div class="card-body">
                        <h5 class="card-title">
                           <span class="d-flex justify-content-between ">
                                {{ item.title }}
                                <i class="fa fa-info-circle"></i>
                            </span>
                        </h5>
                        <p class="card-text">
                            {{ item.event }} <br> {{ item.date }}
                        </p>
                    </div>
                </div>
            </div>
        </div>
        <router-link class="btn btn-outline-primary" to="workspace"> See More </router-link>
    </div>
</template>

<script>
import talksData from '@/assets/data/talks.json'
export default {
    data() {
        return {
            talksData,
            homePageTalks: talksData.techtalks.slice(0,4)
        }
    }
}
</script>