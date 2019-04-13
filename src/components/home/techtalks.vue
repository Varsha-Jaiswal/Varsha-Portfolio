<template>
    <div class="container-fluid">
        <hr><br>  
        <h3>Tech Talks</h3>
        <br><hr>
        <div class="row" v-if="!showTalks">
            <div class="col-md-4" v-for="(item, i) in homePageTalks" :key="i"> 
                <div class="card m-2 btn-outline-primary">
                    <div class="card-body">
                        <h3 class="card-title text-muted">
                            {{ item.name }}
                        </h3>
                        <p class="card-text">
                            {{ item.event }}
                            {{ item.year }}
                        </p>
                    </div>
                </div>
            </div>
        </div>
        <button class="btn btn-primary" v-if="showButton" item-align="right" v-on:click="ShowTalks">See more</button>
        <div class="row" v-if="showTalks">
            <div class="col-md-4" v-for="(item, i) in talksData.techtalks" :key="i"> 
                <div class="card btn-outline-primary m-2">
                    <div class="card-body">
                        <h3 class="card-title text-muted">
                            {{ item.name }}
                        </h3>
                        <p class="card-text">
                            {{ item.event }}
                            {{ item.year }}
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
            homePageTalks: talksData.techtalks.slice(0,3)
        }
    },
    methods: {
        ShowTalks() {
            this.showTalks = !this.showTalks,
            this.showButton = !this.showButton
        }
    }
}
</script>

