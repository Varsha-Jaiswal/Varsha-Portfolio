<template>
  <div class="home">
    <HomeStartScreen></HomeStartScreen>
    <Experiences></Experiences>
    <Skills></Skills>
    <Projects></Projects>
    <TechTalks></TechTalks>
  </div>
</template>

<script>
// @ is an alias to /src
import HomeStartScreen from '@/components/home/homeStartScreen.vue'
import Experiences from '@/components/home/experiences'
import Skills from '@/components/home/skills'
import Projects from '@/components/home/projects'
import TechTalks from '@/components/home/techtalks'

export default {
  name: 'home',
  components: {
    HomeStartScreen,
    Experiences,
    Skills,
    Projects,
    TechTalks
  }
}
</script>
