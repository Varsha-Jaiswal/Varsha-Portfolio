<template>
    <div class="container-fluid">
        <br><br>
        <div class="row">
            <div class="col">
                <h3 class="text-muted text-center">
                    Work Experiences
                </h3>
                <div class="row" v-for="(item, i) in experiencesData.workexperiences" :key="i">
                    <div class="card m-2">
                        <div class="card-body">
                            <h4 class="card-title font-weight-bold text-muted">{{ item.name }}</h4>
                            <hr>
                            <p>{{ item.role }} | {{ item.duration }}</p>
                            <p>{{ item.description }}</p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col">
                <h3 class="text-muted text-center">
                    Community Experiences
                </h3>
                <div class="row" v-for="(item, i) in experiencesData.communityexperiences" :key="i">
                    <div class="card m-2">
                        <div class="card-body">
                            <h4 class="card-title font-weight-bold text-muted">{{ item.name }}</h4>
                            <hr>
                            <p>{{ item.role }} | {{ item.duration }}</p>
                            <p>{{ item.description }}</p>
                        </div>
                    </div>
                </div>
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

