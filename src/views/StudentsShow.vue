<template>
  <div class="students-show">
      <div>
        <br>
        <br>
        <h1>{{ user.first_name }} {{user.last_name}}</h1>
        <img class="show-image" v-bind:src="user.photo" v-bind:alt="user.first_name"/>
        <a href="#" class="btn btn-primary">Contact Info</a> <br> <br>
        
        <span>{{ user.email }}</span>
        <span>{{ user.phone }}</span>
      </div>

      <section id="short-bio">
        <p>{{ user.short_bio }}</p>

      </section>
      
      <section id='experience' v-for="experience in user.experiences">
        <span id="start_date">{{ experience.start_date }}</span><br>
        <span id="end_date">{{ experience.end_date }}</span><br>
        <span id="job_title">{{ experience.job_title }}</span><br>
        <span id="company_name">{{ experience.company_name }}</span><br>
        <span id="details">{{ experience.details }}</span><br>

      </section>
      <section id='education' v-for="education in user.educations">
        <span id="start_date">{{ education.start_date }}</span><br>
        <span id="end_date">{{ education.end_date }}</span><br>
        <span id="degree">{{ education.degree }}</span><br>
        <span id="university_name">{{ education.university_name }}</span><br>
        <span id="details">{{ education.details }}</span><br>

      </section>
      <section id='projects' v-for="project in user.projects">
        <span id="name">{{ project.name }}</span><br>
        <span id="description">{{ project.description }}</span><br>
      
      </section>
      <section id='skills' v-for="skill in user.skills">
        <span id="name">{{ skill.name }}</span> <br>
      </section>
      <section id='twitter'>
        <a class="twitter-timeline" href="https://twitter.com/{TwitterDev}?ref_src=twsrc%5Etfw" >Tweets by TwitterDev</a> 
      </section>
      
  </div>
</template>

<style>
.show-image {
  border-radius: 50%;
  padding: 1em;
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 20%;
}
</style>

<script>
import axios from "axios";

export default {
  data: function () {
    return {
      user: {},
    };
  },
  created: function () {
    axios.get("/api/users/" + this.$route.params.id).then((response) => {
      console.log("users show", response);
      this.user = response.data;
    });
    let twitterScript = document.createElement("script");
    twitterScript.setAttribute("src", "https://platform.twitter.com/widgets.js");
    document.head.appendChild(twitterScript);
  },
  methods: {},
};
</script>