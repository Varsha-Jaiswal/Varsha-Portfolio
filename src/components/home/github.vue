<template>
    <div class="container-fluid">
        <div class="row">
            <div class="col-md-12">
                <h3>GitHub Data</h3>

                <p v-if="showLoader">
                    <img src="https://i.gifer.com/7plQ.gif" width="10%" alt="" srcset="">
                </p>
                <p v-else>
                    {{ githubData }}
                </p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            github: "varsha-jaiswal",
            showLoader: true,
            githubData: {}
        }
    },
    methods: {

    },
    created() {
        fetch('https://api.github.com/users/varsha-jaiswal')
        .then(res => res.json())
        .then(data=>{
            this.showLoader = false
            this.githubData = data
        })
    }
}
</script>
