<template>
  <div class="home">
    <HomeStartScreen @ShowGitHubData="showGitHubData=!showGitHubData"></HomeStartScreen>
    <Github v-if="showGitHubData"></Github>
    <Experiences></Experiences>
    <Skills></Skills>
    <Projects></Projects>
  </div>
</template>

<script>
// @ is an alias to /src
import HomeStartScreen from '@/components/home/homeStartScreen.vue'
import Experiences from '@/components/home/experiences'
import Github from '@/components/home/github'
import Skills from '@/components/home/skills'
import Projects from '@/components/home/projects'

export default {
  name: 'home',
  components: {
    HomeStartScreen,
    Experiences,
    Github,
    Skills,
    Projects
  },
  data() {
    return {
      showGitHubData: false
    }
  }
}
</script>
