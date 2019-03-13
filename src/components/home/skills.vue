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

