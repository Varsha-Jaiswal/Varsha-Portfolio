<template>
    <div class="container-fluid my-5">
        <h3 class="h3-responsive text-muted"><i class="fab fa-autoprefixer"></i> Projects</h3>
        <hr>
        <div class="row mt-4">
            <div class="col-md-4" v-for="(item, i) in homePageProjects" :key="i" > 
                <div class="card m-1 z-depth-0" style="border:1px solid #bdbdbd ">
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
        <router-link class="btn btn-outline-primary z-depth-0 btn-sm mt-3" to="workspace"> See More </router-link>
    </div>
</template>


<script>
import projectsData from '@/assets/data/projects.json'
export default {
    data() {
        return {
            projectsData,
            homePageProjects: projectsData.projects.slice(0,3)
        }
    }
}
</script>

