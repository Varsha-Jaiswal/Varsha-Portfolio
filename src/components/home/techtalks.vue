<template>
    <div class="container-fluid">
        <hr><br>  
        <h3>Tech Talks</h3>
        <br><hr>
        <div class="row" v-if="!showTalks">
            <div class="col-md-6" v-for="(item, i) in homePageTalks" :key="i"> 
                <div class="card m-2">
                    <div class="card-body">
                        <h3 class="card-title text-muted">
                           <span class="d-flex justify-content-between text-muted">
                                {{ item.title }}
                                <i class="fa fa-info-circle" v-on:click="TalkDetails"></i>
                            </span>
                        </h3>
                        <p class="card-text">
                            {{ item.event }}<br>
                            {{ item.date }}
                        </p>
                    </div>
                </div>
            </div>
        </div>
        <button class="btn btn-primary" v-if="showButton" item-align="right" v-on:click="ShowTalks">See more</button>
        <div class="row" v-if="showTalks">
            <div class="col-md-6" v-for="(item, i) in talksData.techtalks" :key="i"> 
                <div class="card m-2">
                    <div class="card-body">
                        <h3 class="card-title text-muted">
                            <span class="d-flex justify-content-between text-muted">
                                {{ item.title }}
                                <i class="fa fa-info-circle" v-on:click="TalkDetails"></i>
                            </span>
                        </h3>
                        <p class="card-text">
                            {{ item.event }}<br>
                            {{ item.date }}
                        </p>
                    </div>
                </div>
            </div>
        </div>
        <button class="btn btn-primary" v-if="!showButton" item-align="right" v-on:click="ShowTalks">See less</button>
    </div>
</template>


<script>
import talksData from '@/assets/data/talks.json'
export default {
    data() {
        return {
            talksData,
            showTalks:false,
            showButton: true,
            homePageTalks: talksData.techtalks.slice(0,4)
        }
    },
    methods: {
        ShowTalks() {
            this.showTalks = !this.showTalks,
            this.showButton = !this.showButton
        },
        TalkDetails() {
            
        }
    }
}
</script>

