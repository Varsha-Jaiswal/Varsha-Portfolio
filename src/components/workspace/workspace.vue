<template>
    <div class="container-fluid">
        <hr><br>  
        <h3>Projects</h3>
        <br><hr>
        <router-link class="btn btn-outline-primary" to="/"> Back to Home </router-link>
        <div class="row">
            <div class="col-md-6" v-for="(item, i) in projectsData.projects" :key="i"> 
                <div class="card btn-outline-primary m-2">
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
        <hr><br>  
        <h3>Tech Talks</h3>
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
        <router-link class="btn btn-outline-primary" to="/"> Back to Home </router-link>
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