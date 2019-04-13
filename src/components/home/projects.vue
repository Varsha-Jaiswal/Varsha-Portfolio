<template>
    <div class="container-fluid">
        <hr><br>  
        <h3>Projects</h3>
        <br><hr>
        <div class="row">
            <div class="col-md-4" v-for="(item, i) in homePageProjects" :key="i"> 
                <div class="card m-2 btn-outline-primary">
                    <div class="card-body">
                        <h3 class="card-title text-muted">
                            {{ item.name }}
                        </h3>
                        <p class="card-text">
                            {{ item.description }}
                        </p>
                        <a :href="item.projectUrl" target="_blank">See Project >></a>
                    </div>
                </div>
            </div>
        </div>
        <router-link class="btn btn-outline-primary" to="workspace"> See More </router-link>
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

