<template>
    <div align="center">
        <h1>Varsha </h1><hr>
        <p class="text-muted">Lorem ipsum dolor sit amet consectetur adipisicing elit. Dignissimos molestiae sequi enim quo aspernatur dolores soluta, vitae omnis delectus eligendi, beatae consequuntur incidunt obcaecati saepe aut impedit nesciunt! Laborum, ipsam.</p>
        <button class="btn btn-primary" v-on:click="showData">Show Github Data</button>
    </div>
</template>

<script>
export default {
    methods: {
        showData() {
            this.$emit('ShowGitHubData')
        }
    }
}
</script>


