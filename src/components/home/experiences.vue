<template>
    <div class="container-fluid">
        <br><br>
        <div class="row">
            <div class="col-md-6 col-12">
                <h3 class="text-muted h3-responsive">
                   <i class="fab fa-autoprefixer"></i> Work Experiences
                </h3>
                <div class="row" v-for="(item, i) in experiencesData.workexperiences" :key="i">
                    <div class="card m-0 z-depth-0">
                        <div class="card-body">
                            <h4 class="card-title font-weight-bold text-muted h4-responsive" style="max-height:200">{{ item.name }}</h4>
                            <hr>
                            <div v-if="item.role2 && item.duration2">
                                <p style="color:blue">{{ item.role1 }} | {{ item.duration1 }}</p>
                                <p>{{ item.description1 }}</p>
                                <p style="color:blue"> {{ item.role2 }} | {{ item.duration2 }}</p>
                                <p>{{ item.description2 }}</p>
                            </div>
                            <div v-else>
                                <p style="color:blue">{{ item.role1 }} | {{ item.duration1 }} </p>
                                <p>{{ item.description1 }}</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col-md-6 col-12">
                <h3 class="text-muted h3-responsive">
                   <i class="fab fa-autoprefixer "></i> Community Experiences
                </h3>
                <div class="row" v-for="(item, i) in experiencesData.communityexperiences" :key="i">
                    <div class="card m-0 z-depth-0">
                        <div class="card-body">
                            <h4 class="card-title font-weight-bold text-muted h4-responsive">{{ item.name }}</h4>
                            <hr>
                            <div v-if="item.role2 && item.duration2">
                                <p style="color:blue">{{ item.role1 }} | {{ item.duration1 }}</p>
                                <p>{{ item.description1 }}</p>
                                <p style="color:blue">{{ item.role2 }} | {{ item.duration2 }}</p>
                                <p>{{ item.description2 }}</p>
                            </div>
                            <div v-else>
                                <p style="color:blue">{{ item.role1 }} | {{ item.duration1 }} </p>
                                <p>{{ item.description1 }}</p>
                            </div>
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

