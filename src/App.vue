<template>
  <transition name="fade" tag="div" class="wrapper" mode="out-in">
    <div class="wrapper" v-if="isLoaded" id="app">
      <LandingPage />
      <!-- <Description :user="userData.user" :content="userData.description" :links="userData.links" /> -->
      <!-- <Experience :content="userData.experiences" /> -->
      <Skills :skills="userData.bucket.objects[4]" />
      <Projects :projects="userData.bucket.objects[5].metafields[0].value" />
      <Footer :user="userData" :links="userData.links" />
    </div>
  </transition>
</template>

<script>

import LandingPage from "./components/LandingPage.vue";
// import Description from "./components/Description.vue";
// import Experience from "./components/Experience.vue";
import Skills from "./components/Skills.vue";
import Projects from "./components/Projects.vue";
import Footer from "./components/Footer.vue";

import userData from "../data/data.json";

export default {
  name: "App",

  components: {
    LandingPage,
    // Description,
    // Experience,
    Skills,
    Projects,
    Footer,
  },
  data: () => ({
    isLoaded: true,

  }),
  computed: {
    userData() {
      // console.log("Yeyy ==>. ", userData.bucket.objects);
      return userData
    }
  },
  methods: {
  },
  created() {
    // document.body.classList.add("loading");

    // Promise.all([this.fetchPosts(), this.fetchSkills(), this.fetchProjects(), this.fetchUser()]).then(([posts, skills, projects, user_data]) => {
    //   user_data = this.extractFirstObject(user_data);
    //   this.posts = posts.objects;
    //   console.log("user skills ==>> ", projects.objects)
    //   this.skills = skills.objects;
    //   this.projects = projects.objects;
    //   this.user = {
    //     name: user_data.metadata.name,
    //     status: user_data.metadata.status,
    //     email: user_data.metadata.email,
    //     phone: user_data.metadata.phone,
    //     city: user_data.metadata.city,
    //     lang: user_data.metadata.lang,
    //     photo: user_data.metadata.photo,
    //   }
    //   this.isLoaded = true;
    //   this.$nextTick(() => document.body.classList.remove("loading"));
    // });
  },
};
</script>

<style scoped lang="scss">
@import "./styles/constants.scss";

#app {
  font-family: Montserrat-Regular, serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

.wrapper {
  height: 100%;
}
</style>
