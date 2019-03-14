<template>
    <div class="container-fluid">
        <hr><br>  
        <h3>Skills Set</h3>
        <br><hr>
        <div class="row">
            <div class="col-md-2" v-for="(item, i) in skillsData.skills" :key="i">
                <p class="text-muted">
                    {{ item.name }}
                </p>
                <div class="progress">
                <div class="progress-bar" role="progressbar" v-bind:style="{ width: item.rating }" aria-valuemin="0" aria-valuemax="100"></div>
                </div>
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

