<template>
  <div class="home">
    <nav>
      <a href="#hello">Hello</a>
      <a href="#mywork">Projects</a>
      <a href="#skills">Skills</a>
      <a href="#contact">Contact</a>
    </nav>

    <router-view />
    <HelloWorld />
    <MyWork />
    <MySkills />
    <ContactMe />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import MyWork from '@/components/MyWork.vue'
import MySkills from '@/components/MySkills.vue'
import ContactMe from '@/components/ContactMe.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld,
    MyWork,
    MySkills,
    ContactMe
  }
}
</script>
