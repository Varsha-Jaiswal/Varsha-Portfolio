<template>
    <div>
        <ul class="list-group list-group-horizontal" type="none">
            <li v-for="(item, i) in portfolioData.portfolioData.socialMediaProfiles" :key="i">
                <a :href="item.url" target="_blank" class="fb-ic mr-3" style="color:black; " role="button">
                    <i :class="item.icon"></i>
                </a>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    props:{
        portfolioData: {}
    },
}
</script>
