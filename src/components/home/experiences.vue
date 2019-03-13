<template>
    <div class="container-fluid">
        <div class="row">
            <div class="col-md-12">
                <h2 class="text-muted">My Experiences</h2><hr>
            </div>
        </div>
        <div class="row">
            <div class="col-md-6" v-for="(item, i) in experiencesData.experiences" :key="i">
                <h3>
                    {{ item.name }}
                </h3>
                <p class="text-muted">
                    {{ item.role }} | {{ item.duration }}
                </p>
                <p>
                    {{ item.description }}
                </p>
            </div>
        </div>
    </div>
</template>


<script>
import experiencesData from '@/assets/data/experiences.json'
export default {
    data() {
        return {
            experiencesData
        }
    }
}
</script>

