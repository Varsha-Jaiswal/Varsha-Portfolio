<template>
    <div class="container-fluid">
        <hr><br>  
        <h3>Projects</h3>
        <br><hr>
        <div class="row">
            <div class="col-md-4" v-for="(item, i) in projectsData.projects" :key="i"> 
                <h3 class="text-muted">
                    {{ item.name }}
                </h3>
                <p>
                    {{ item.year }} | <a v-bind:href= "item.project-url">Show Project</a>
                </p>
                <p>
                    {{ item.description }}
                </p>
            </div>
        </div>
    </div>
</template>


<script>
import projectsData from '@/assets/data/projects.json'
export default {
    data() {
        return {
            projectsData
        }
    }
}
</script>

