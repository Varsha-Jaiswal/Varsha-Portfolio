<template>
    <div class="container-fluid my-5">
        
        <h3 class="h3-responsive text-muted"><i class="fab fa-autoprefixer"></i> Skills Set</h3>
        <hr>
        <div class="row mt-5">
            <div class="col-md-2" v-for="(item, i) in skillsData.skills" :key="i">
                <p class="text-muted">
                    {{ item.name }}
                </p>
                <div class="progress">
                <div class="progress-bar" role="progressbar" v-bind:style="{ width: item.rating }" aria-valuemin="0" aria-valuemax="100"></div>
                </div>
                <br>
            </div>
        </div>
    </div>
</template>


<script>
import skillsData from '@/assets/data/skills.json'
export default {
    data() {
        return {
            skillsData
        }
    }
}
</script>

