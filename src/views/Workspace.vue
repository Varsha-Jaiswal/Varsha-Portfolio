<template>
  <div class="workspace">
    <Projects></Projects> 
    <TechTalks></TechTalks>
  </div>
</template>
<script>
import Projects from '@/components/home/projects'
import TechTalks from '@/components/home/techtalks'

export default {
  name: 'workspace',
  components: {
    Projects,
    TechTalks
  },  
}
</script>
