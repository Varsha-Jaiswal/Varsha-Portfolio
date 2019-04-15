<template>
    <div class="container-fluid my-5">
        <h3 class="h3-responsive text-muted"><i class="fab fa-autoprefixer"></i> Tech Talks</h3>
        <hr>
        <div class="row mt-3 p-3">
            <div class="col-md-4 p-1" v-for="(item, i) in homePageTalks" :key="i" > 
                <div class="z-depth-0" style="border:1px solid #bdbdbd;border-radius:5px ">
                    <div class="card-body">
                        <h5 class="card-title my-0 h5-responsive">
                           <span class="d-flex justify-content-between ">
                                {{ item.title }}
                            </span>
                        </h5>
                        <p class="card-text text-muted">
                            {{ item.event }} <br> {{ item.date }}
                        </p>
                    </div>
                </div>
            </div>
        </div>
        <router-link class="btn btn-outline-primary m-0 z-depth-0 btn-sm" to="workspace"> See More </router-link>
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