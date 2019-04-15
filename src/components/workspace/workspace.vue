<template>
    <div class="container-fluid my-5">
        
        <div class="row">
            <div class="col-md-12 p-0">
                <h3 class="h3-responsive"><i class="fab fa-autoprefixer"></i> Projects</h3>
            </div>

            <div class="col-12 col-md-6 p-1" v-for="(item, i) in projectsData.projects" :key="i"> 
                <div class="m-0" style="border:1px solid #bdbdbd;border-radius:5px">
                    <div class="card-body">
                        <h4 class="card-title text-muted h4-responsive">
                            {{ item.name }}
                        </h4>
                        <p class="card-text">
                            {{ item.description }}
                        </p>
                        <a :href="item.projectUrl" target="_blank">See Project >></a>
                    </div>
                </div>
            </div>
        
        </div>

        <div class="row my-5">
            <div class="col-md-12 p-0">
                <h3 class="h3-responsive"><i class="fab fa-autoprefixer"></i> Talks</h3>
            </div>

            <div class="col-12 col-md-6 p-1" v-for="(item, i) in talksData.techtalks" :key="i"> 
                <div class="m-0" style="border:1px solid #bdbdbd;border-radius:5px">
                    <div class="card-body">
                        <h4 class="card-title text-muted h4-responsive mb-0">
                             <span class="d-flex justify-content-between">
                                {{ item.title }}
                            </span>
                        </h4>
                        <p class="card-text">
                            {{ item.event }} <br> {{ item.date }}
                        </p>
                    </div>
                </div>
            </div>
        
        </div>


         
        <!-- <h3>Tech Talks</h3>
        <br><hr>
        <div class="row">
            <div class="col-md-6" v-for="(item, i) in talksData.techtalks" :key="i"> 
                <div class="card m-2">
                    <div class="card-body">
                        <h5 class="card-title">
                            <span class="d-flex justify-content-between">
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
        <router-link class="btn btn-outline-primary" to="/"> Back to Home </router-link> -->
    </div>
</template>

<script>
import talksData from '@/assets/data/talks.json'
import projectsData from '@/assets/data/projects.json'

export default {
    data() {
        return {
            talksData,
            projectsData
        }
    }
}
</script>