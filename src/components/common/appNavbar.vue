<template>
    <nav class="navbar navbar-expand-lg navbar-light bg-white">
        <div class="container">
        <a class="navbar-brand" href="#">{{data.jsonObj.name}}</a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>

        <div class="collapse navbar-collapse" id="navbarSupportedContent">
            <ul class="navbar-nav mr-auto">
                <li class="nav-item" v-for="(item,i) in myData.navbarLinks" :key="i">
                    <router-link class="nav-link" :to="item.Link">{{ item.LinkName }}</router-link>
                </li>
            </ul>
        </div>
        </div>
    </nav>
</template>

<script>
import navData from '@/assets/data/data.json'
export default {
    props:{
        data: {
            jsonObj: {}
        }
    },
    data() {
        return {
            myData : navData
        }
    }
}
</script>


