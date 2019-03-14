<template>
    <div class="container-fluid">
        <hr><br>  
        <h3>Projects</h3>
        <br><hr>
        <div class="row" v-if="!showProjects">
            <div class="col-md-4" v-for="(item, i) in homePageProjects" :key="i"> 
                <div class="card">
                    <div class="card-body">
                        <h3 class="card-title text-muted">
                            {{ item.name }}
                        </h3>
                        <p class="card-text">
                            {{ item.description }}
                        </p>
                        <a :href= "item.project-url">Show Project</a>
                    </div>
                </div>
            </div>
        </div>
        <button class="btn btn-primary" v-if="showButton" item-align="right" v-on:click="ShowProjects">See more</button>
        <div class="row" v-if="showProjects">
            <div class="col-md-4" v-for="(item, i) in projectsData.projects" :key="i"> 
                <div class="card m-2">
                    <div class="card-body">
                        <h3 class="card-title text-muted">
                            {{ item.name }}
                        </h3>
                        <p class="card-text">
                            {{ item.description }}
                        </p>
                        <a :href= "item.project-url">Show Project</a>
                    </div>
                </div>
            </div>
        </div>
        <button class="btn btn-primary" v-if="!showButton" item-align="right" v-on:click="ShowProjects">See less</button>
    </div>
</template>


<script>
import projectsData from '@/assets/data/projects.json'
export default {
    data() {
        return {
            projectsData,
            showProjects:false,
            showButton: true,
            homePageProjects: projectsData.projects.slice(0,3)
        }
    },
    methods: {
        ShowProjects() {
            this.showProjects = !this.showProjects,
            this.showButton = !this.showButton
        }
    }
}
</script>

